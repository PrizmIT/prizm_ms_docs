# Project Controls

Project Controls is the project-level workspace under **Projects → (project) → Project Controls**. It groups Plan, WBS & Progress, QS Support, Cost Plan, Approval review and Funding. This page records confirmed, step-by-step work done in Project Controls, starting with project P1155.

## P1155 — Confirmed Steps

### 1. Purpose

This page records every step of the P1155 investigation (Project 151, Shaft 1 & 2 – MOT) that has been **completed and confirmed in the live system**. It is the working log for the team: what was done, where, and what the result was. Only confirmed steps appear here. Planned or unconfirmed work is listed separately at the end.

The goal of the investigation is to make purchase order **PEG-PO-26110011** (PR-26110009) approvable through the normal approval engine, without bypassing approvals or losing history.

| Step | Name | Status |
|---|---|---|
| 1–4 | Identify the PO → PR → RR → budget chain, history, hashes and the cause of the stale scope | Done (diagnosis) |
| 5 | Review the governing scope and correct the Cost Plan / WBS planning | Done |
| 6 | Financial approval through the original approvers + funding reconciliation | Done |
| 7 | PO approval and release checks | **In progress** |

### 2. Confirmed steps — 11 November 2026

#### 2.1 Owner and reference fields became searchable lists

- **Where:** Project Controls → Plan → **Governing Scope Review**.
- **What changed:** the assumption **Owner** is chosen from a searchable list of active staff, and the **Assumption reference** from a searchable list of the work package's verified drawing revisions. The server refuses an inactive owner or an unlisted reference.
- **Release:** prizm_project 1.101.0 (pull requests #3376 and #3377), deployed to staging and production.

#### 2.2 Governing Scope v4 recorded

- **Where:** Project Controls → Plan → Governing Scope Review.
- **Why:** v3 was out of date only because the task weights of WP 2.2-PS-197 changed on 7 November.
- **PS-201 pedestal:** no new decision was needed. The Owner's assumption recorded in v1, v2 and v3 on drawing P24050-24-85-76-1601 Rev 2C was re-recorded: 1.5 × 0.5 × 1.0 m pedestal = 0.75 m³ plus 3.0 m³ footing = 3.75 m³, owner Mostafa Mohammed.
- **How:** fill Engineering reference, Review reason and the PS-201 assumption → **Preview engineering review** → check all 26 rows → tick the confirmation → **Record reviewed scope**.
- **Result:** Review version **4**, status **Current**, 26 work packages, every quantity unchanged from v3.

#### 2.3 Physical allocations made current (34 allocations, 17 foundations)

- **Where:** Project Controls → QS Support → Planning Review → **Plan operation allocations**.
- **Why:** after a new governing review, each allocation still pointed to the previous review.
- **How:** for each of the 17 foundation work packages, save the same allocation rows again, then confirm the planning review.
- **Result:** 34 allocations, **64.715 m³** in total, all current. Nothing was approved for budget, client or invoice.

#### 2.4 Cost Plan reconciled (revision 48)

- **Where:** Project Controls → Cost Plan → **Review source reconciliation**.
- **Problem:** the 34 concrete cost rows were held, and the reconciliation was blocked with ALLOWANCE_SOURCE.
- **Fix:** the reconciliation now re-links a cost row to the current allocation review when the task, component, quantity, unit and drawing file are unchanged (prizm_project 1.102.0, pull requests #3382 and #3383).
- **Result:** Cost Plan **revision 48**, 34 rows re-linked, none held, mapped value unchanged at AED 595,395.58. Still a draft.

#### 2.5 All lines of budgets #790 and #794 mapped (revision 49)

- **Where:** Project Controls → Cost Plan.
- **How:** each of the 51 unmapped lines was mapped following how the same item is already mapped in other P1155 budgets: shared materials to the project pools, PPE to 1.3, plant to 1.4, services to 1.2 and 1.6, overtime to 1.5.
- **Result:** Cost Plan **revision 49**, 213 of 224 lines fully mapped, mapped value AED 822,609.58. The 10 remaining lines are recorded monetary-only balances from other budgets. Still a draft; nothing financially approved.

#### 2.6 New resource requests work again for nested budgets

- **Problem:** Eng. Mostafa could not add Backhoe or Overtime Pay to a new resource request. The message was "This budget source needs reconciliation before a new RR can consume it", but the real cause was a defect: the item list ignored an additional budget placed under the selected budget when that budget has its own parent.
- **Fix:** prizmbudget 1.47.2 (pull requests #3387 and #3388), deployed to production.
- **Result:** Backhoe 1 of 1, Overtime Pay 55 of 55 and Overtime Pay for Sahara JP & HSE 25 of 25 are available. Ready Mix stays at 111.5 of 131.5 m³.

##### How to create a resource request for P1155

1. Open the request type: [Material](https://ms.prizm-energy.com/MS/admin/prizmbudget/resource_request/1) · [Manpower](https://ms.prizm-energy.com/MS/admin/prizmbudget/resource_request/2) · [Equipment](https://ms.prizm-energy.com/MS/admin/prizmbudget/resource_request/3) · [Service](https://ms.prizm-energy.com/MS/admin/prizmbudget/resource_request/6).
2. **Budget:** choose **P1155 - Preliminary budget including the required materials to complete the project**. Do not choose a **WBS budget draft** or **Budget for Shaft 1 & 2**.
3. **Budget / additional budgets:** choose the budget that holds the item, for example **Initial project budget**.
4. **Budget Items:** select the items, then **Add selected items**.
5. Enter the required quantities → **Save draft** → **Submit for approval** on the next screen.

#### 2.7 Native WBS draft compiled

- **Where:** Project Controls → WBS & Progress → **Native WBS budget**.
- **Result:** a new draft built from Cost Plan revision 49, covering all 224 source lines (213 of them fully mapped). No "unallocated scope" problem. Draft only; nothing approved.

#### 2.8 Two lines with unit N/A recorded as money-only

- **Where:** Project Controls → Cost Plan.
- **Why:** two lines in **Initial project budget** — **Accommodation, Engineers, Monthly** (AED 1,320) and **Trailer Rental 30–35 Tonne** (AED 4,500) — have unit N/A, which blocks approval.
- **How:** recorded as whole-line money amounts, the same way this project already records **Worker Accommodation** and **Bus Rental**. They stay mapped to their work packages.
- **Result:** Cost Plan **revisions 50 and 51**. Nothing approved; their budget capacity stays held.

#### 2.9 Native WBS draft rebuilt

- **Result:** a new draft built from Cost Plan revision 51. The unit N/A problem is gone.

#### 2.10 Cost review submitted

- **Where:** Project Controls → Approval review → **Submit for review**.
- **Result:** status **Submitted for review**. The financial check is ready with no blockers. The concrete line's specification check and three funding items (a pairing of AED 92,334, a deficit of AED 32,634, and an overdraw of AED 5,640) are tracked separately and handled later in Step 6.

#### 2.11 Cost approval for draft #796 approved and applied

- **Problem:** **Submit cost approval** failed with a general error (EXEC_TRANSACTION). The Approvals module refused to route it through the Budget policy.
- **Fix:** Project Controls approvals now have their own document type, **Project Controls** (pull requests #3419 and #3420: prz_approvals 1.21.1, prizmbudget 1.48.1, prizm_project 1.106.0). A failed save now shows its reason in a red alert and is written to the Activity Log.
- **Setup on production:** in Approvals → Settings: stage **Project Controls**, status **Project Controls Approval**, and policy **Project Controls Approval — Project** (Context Type Project, approver Role Project Senior Manager, required).
- **Decision:** request **#3** was routed to the Project Senior Manager, Mostafa Mohammed. He approved via **Microsoft Teams**, and Mustafa Zaroug recorded the decision on his behalf. The step reads "Decided by Mustafa Zaroug on behalf of Mostafa Mohammed", and the Activity Log holds the entry.
- **Result:** draft #796 is **APPROVED** and its cost baseline is applied.
- **Note:** an opportunity's WBS or CBS has no project, so it does not use this policy. It needs its own Project Controls policy with a Department or General context.

#### 2.12 Funding reconciled again on the new baseline

- **Where:** Project Controls → Approval → **Funding trail**.
- **Why:** the funding reconciliation approved on 3 November (version 2) became **Stale** when the new cost baseline was approved, and purchase orders were held (PURCHASE_SOURCE_SPENDING_HELD).
- **How:** the suggested worksheet matched version 2 exactly, so it was submitted unchanged (**Submit worksheet**, version 3) and approved (**Approve submitted worksheet**, version 4). No new value was assumed.
- **Values:** releases AED 59,700; new budget-funding authority AED 32,634; draw correction −AED 5,640 on line #7768. Not bank cash.
- **Result:** the spending gate is ready with no blockers.

#### 2.13 Purchase order PEG-PO-26110011 approved

- **Where:** Prizm Purchase → the purchase order → **Approver And Stages Info**.
- **Result:** Mostafa Mohammed's step "Projects - UAE Suppl" approved at 16:02, recorded by Mustafa Zaroug on his behalf ("Delegated Action By"). AED 8,232 to Gulf Ready Mix Fujairah: water AED 240 and C40 concrete AED 7,600, plus VAT.

### 3. Confirmed steps — 12 November 2026

#### 3.1 Helper #7956 withdrawn from its monetary-only hold

- **Where:** Project Controls → Cost Plan → source allowance for **Helper #7956** (budget #734, 400 M.DAY × AED 150).
- **Why:** this line had been held as monetary-only since 25 October 2026 ("helper M.DAY vs existing MH capacity reconciliation"), so it did not appear as requestable in a Manpower resource request.
- **Decision:** the project owner, Mustafa Zaroug, decided to release it → **Withdraw**.
- **Result:** Cost Plan **revision 52**. Withdrawing alone leaves the line unallocated (SCOPE_UNALLOCATED) and still blocks spending until it is mapped again (see 3.2).

#### 3.2 Helper #7956 mapped as a day-rate service line (revision 53)

- **Where:** Project Controls → Cost Plan.
- **How:** mapped to the project pool as a day-rate line — resource family **SERVICE**, CBS **"S"**, Project Pool, full 400 quantity — the same pattern already used for **Labour Accommodation #7768** (days). It could not become a Manpower pool line, because a Manpower pool line must be in MANHOUR, and Helper is recorded in M.DAY.
- **Result:** Cost Plan **revision 53**.

#### 3.3 Native WBS draft recompiled (draft #797, revision 30)

- **Where:** Project Controls → WBS & Progress → **Native WBS budget**.
- **Result:** draft **#797, revision 30**. Cost review submitted.

#### 3.4 Cost approval applied — new baseline

- **Where:** Project Controls → Approval review.
- **Decision:** request **#4** (policy #2, Project Controls) was approved by the project owner, Mustafa Zaroug, on behalf of Eng. Mostafa Mohammed. The record notes an **owner decision**, not an approval given through Microsoft Teams.
- **Result:** status **APPLIED**. Draft #797 is now the approved cost baseline.

#### 3.5 Funding reconciled again on the new baseline

- **Where:** Project Controls → Approval → **Funding trail**.
- **Why:** the new cost baseline made the funding reconciliation stale and held purchase orders (PURCHASE_SOURCE_SPENDING_HELD).
- **How:** re-recorded unchanged from the approved plan: **Submit worksheet** (version 5), **Approve submitted worksheet** (version 6).
- **Result:** the spending gate is ready with no blockers; purchase orders are not held.

#### 3.6 Helper now shows as requestable (checked, not saved)

- **Where:** **New → Manpower resource request** → Budget **"P1155 - Budget for Shaft 1 & 2"** → Budget Items.
- **Result:** Budget Items now shows **Helper · M.DAY · 400**. Opening **Add selected items** shows unit price AED 150, total 400, and 394 available (6 already held by an earlier request). This was checked only; nothing was saved.

#### 3.7 Eng. Mostafa and Eng. Osama informed

- Eng. Mostafa Mohammed and Eng. Osama were told about this on Microsoft Teams.
- **Still open:** whether the 400 helper-days are additional to the helper hours already recorded under requests #11336 and #11347, or the same people — Eng. Osama is to confirm. The conversion between M.DAY and MANHOUR (8 hours per day) is not implemented in the system. Until this is confirmed, request helpers from one line only.

#### 3.8 Lesson: a Cost Plan change after approval needs a full cycle

A Cost Plan change made after a cost approval does not take effect by itself. Before purchase orders can be released again, repeat in order: recompile the Native WBS draft → submit it for review → get cost approval → re-record funding (submit, then approve).

### 4. When a PO is held after a new cost approval

This will happen again. A funding reconciliation is tied to the cost baseline it was approved on, so **every** new cost approval makes it Stale and holds every purchase order of the project with the message "PO approval is on hold…" (PURCHASE_SOURCE_SPENDING_HELD). Nothing is saved; the PO waits at its step.

To release it (administrator with Project Controls budget review permission):

1. Open the project → **Project Controls → Approval → Funding trail**. It shows **Stale**.
2. Compare the suggested worksheet with the last approved version. When nothing changed, it repeats the approved plan.
3. Tick the confirmation, write a reason → **Submit worksheet**.
4. Write the approval reason → **Approve submitted worksheet**.
5. Go back to the purchase order → **Approved**.

If the worksheet shows a real change (a new release, a different amount, a new overdraw), do not approve it as a repeat: the project owner decides first.

### 5. Next, not yet confirmed

- Review the specification hold on concrete source #7775.
- Operational activation (spending authority) remains separate and is not yet granted.
- Confirm with Eng. Osama whether Helper #7956's 400 days are additional to requests #11336/#11347 or the same people; implement the M.DAY ↔ MANHOUR conversion.
