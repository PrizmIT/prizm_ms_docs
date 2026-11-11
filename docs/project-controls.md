# Project Controls

Project Controls is the project-level workspace under **Projects → (project) → Project Controls**. It groups Plan, WBS & Progress, QS Support, Cost Plan, Approval review and Funding. This page records confirmed, step-by-step work done in Project Controls, starting with project P1155.

## P1155 — Confirmed Steps

### 1. Purpose

This page records every step of the P1155 investigation (Project 151, Shaft 1 & 2 – MOT) that has been **completed and confirmed in the live system**. It is the working log for the team: what was done, where, and what the result was. Only confirmed steps appear here. Planned or unconfirmed work is listed separately at the end.

The goal of the investigation is to make purchase order **PEG-PO-26110011** (PR-26110009) approvable through the normal approval engine, without bypassing approvals or losing history.

| Step | Name | Status |
|---|---|---|
| 1–4 | Identify the PO → PR → RR → budget chain, history, hashes and the cause of the stale scope | Done (diagnosis) |
| 5 | Review the governing scope and correct the Cost Plan / WBS planning | **In progress** |
| 6 | Financial approval through the original approvers + funding reconciliation | Not started |
| 7 | PO approval and release checks | Not started |

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

> **Do not approve purchase order PEG-PO-26110011 yet.** It still needs the financial approval of Step 6.

### 3. Next, not yet confirmed

- **Step 5.8:** compile a new Native WBS draft from Cost Plan revision 49. The check shows no SCOPE_UNALLOCATED is expected.
- **Step 6:** send the cost approval to the original approvers, then reconcile funding.
- **Step 7:** approve PEG-PO-26110011 and run the release checks.
