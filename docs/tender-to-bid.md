# Tender to Bid (T2B)

## 1. Introduction

**Tender to Bid (T2B)** is the programme that takes a tender from its documents to a
submitted bid inside the PRIZM ENERGY portal. The work happens in the **Virtual Tendering
Team** of an opportunity: a team of AI agents prepares each stage of the bid (executive
summary, decomposition, technical solution, risk, benchmarking, pricing, legal, proposal and
submission QA), and people approve the result at agreed control points.

This section grows with the programme. Each time a part of the T2B plan is finished, what it
changes for you is added here.

This guide is for:

- Tender and bid managers
- Business Development teams
- Engineers and estimators who review stage outputs
- Managers who approve bids

## 2. Programme progress

| Part | What it delivers | Status |
|---|---|---|
| **Step 0 — Control fixes** | Final human sign-offs can't be switched to Auto, and a hold is released only by a real approval in the current run. | ✅ Closed on 10 November 2026 |
| PH0 — Diagnose & freeze | Shows where bids actually wait and on whom, with a frozen specification. | In progress |
| PH1 — Right approver, right wait | Each decision goes to the right person, with a clear waiting time. | Planned |
| P00–P06 | The bid stages themselves, from foundation to submission. | Planned |

## 3. Where to find it

Open an opportunity and select the **Virtual Tendering Team** tab.

![Virtual Tendering Team tab](./tender-to-bid/img/vtt_overview.png)

- **Run Opportunity** starts a run: the virtual team works through the stages in order and
  pauses only when a person has to decide.
- **Intake & Documents**, **Scope Gate & ITP** and **Briefs** hold the set-up of the
  opportunity.
- Below them, one tab per stage shows its output, and **Decisions** lists what is waiting for
  you.

## 4. Step 0 — Control fixes (what changed for you)

Step 0 makes sure no bid moves past a person who must approve it. It was finished on
10 November 2026.

### 4.1 Control modes (the ITP control matrix)

Every stage has controls, listed in **Scope Gate & ITP → ITP control matrix**. Each control has
one of four modes:

| Mode | Meaning |
|---|---|
| **Auto** | The virtual team carries on without stopping. |
| **WP** (Witness point) | The virtual team carries on and notifies the owner. |
| **HP** (Hold point) | The run stops until a person approves. |
| **NR** | The control is skipped. |

The presets at the top (**All Hold**, **Conservative**, **Witness-heavy**, **Full Auto**) set many
controls at once. The counters on the right show how many controls are in each mode.

![ITP control matrix](./tender-to-bid/img/itp_control_matrix.png)

### 4.2 Final sign-offs always stay on Hold

Five controls are **final human sign-offs**. They stay on **HP** under every preset, including
**Full Auto**, and can't be changed one by one:

| Stage | Control |
|---|---|
| Executive Summary | Human acceptance |
| Benchmarking | Accept benchmarks |
| Pricing / RFQ | Margin and contingency gate |
| Proposal | Human acceptance |
| Submit QA | Human sign-off (statutory gate) |

Every change of a control's mode, and every refused attempt to move a final sign-off off Hold,
is recorded in the TenderOps audit trail.

![Executive Summary holds](./tender-to-bid/img/itp_mandatory_signoff.png)

### 4.3 A hold is released only by an approval in the same run

When a run reaches a Hold point, a decision appears in **Decisions**. Choose
**Release hold — continue** and select **Submit decisions**.

- The approval belongs to **that run only**. If the opportunity is run again later, the same
  hold stops the new run and asks again. An approval from an earlier run never releases a later
  one.
- Only an explicit **Release hold** counts. **Keep on hold** never releases anything.
- A stage can have several holds. Releasing one shows the next; they are not released together.

### 4.4 "Re-approval required after control fix"

Approvals given **before** Step 0 were not tied to a run, so they no longer release a hold. The
first time such a hold comes back, its title ends with **"Re-approval required after control
fix"** and its text names the earlier decision, for example *"decision #5 approved this hold
before the control fix"*.

Approve it again to continue. This happens once per control and opportunity; after that, holds
look normal.

### 4.5 Answering decisions

![Decisions box](./tender-to-bid/img/decisions_box.png)

1. Open the **Decisions** tab. The counter shows how many decisions are waiting.
2. For each decision you want to settle, choose one answer and, if needed, add a note.
3. Select **Submit decisions** once. All your answers are sent together.

There are two kinds of decisions:

| Kind | When it appears | Answers |
|---|---|---|
| **Blocker** (a hold) | The run reached a Hold point. | Release hold — continue · Provide input and re-run this stage · Keep on hold |
| **Escalation** | The virtual team could not close all gaps itself, for example claims without a source. | Provide missing input — re-run stage · Waive gaps and continue with documented risk · Hold pursuit pending clarification |

**Who can answer:** the person the decision is assigned to, and any administrator.

## 5. Frequently asked questions

**I approved this hold yesterday. Why is it asking again?**
Either the opportunity was run again (each run needs its own approval), or your approval was
given before Step 0 (the hold then says "Re-approval required after control fix").

**Can I set the final sign-offs to Auto to save time?**
No. The five final sign-offs stay on Hold under every preset. This is intentional.

**What happens if I choose "Keep on hold"?**
The run stays paused. Nothing moves until someone releases the hold.
