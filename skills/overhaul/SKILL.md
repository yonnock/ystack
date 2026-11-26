---
name: overhaul
description: "Prepare an overhaul as a verified report: parallel analyses of one product, area or module, a fact check against the code, then one HTML page with what must stay, weaknesses, concepts and a staged plan. Read-only. Use when the user asks for an overhaul, a concept for a large change, or the groundwork for a large refactor or a vague large issue."
---

# Overhaul

An overhaul studies one **target** through several **lenses** and ends in a report a person can order work from: "do stages 1 and 2, skip 3". The report is the only product.

## Read-only

Read, build, test and measure. Tracked files, history, running services, deployments, data and the user's machine stay as they were. Builds and tests may fill the folders the repository ignores, such as dependencies and build output. An experiment that needs code lives in a temporary directory outside the repository and is removed afterwards.

## 1. Fix the target

From the conversation and the repository (its agent instructions, README, decision records, open issues on the target), write three lines:

- **Target**: the product, area or module under study.
- **Kind**: an overhaul of what exists, a concept for something new, or a refactor.
- **Decision**: what the user will decide with the report in hand.

Ask only when the target itself is unclear, and then one question. Done when the three lines stand.

## 2. Establish the baseline

Install what the repository documents, then run its documented build and tests. Record each command with its result and duration, the commit, and the plain counts that size the target (files, lines, tests). A documented command that fails or runs nothing is the report's first finding.

Done when every documented check has run, or stands recorded with the error that stopped it or the Read-only reason it was left alone.

## 3. Choose the lenses

A lens is one angle with one question, held by one agent. Choose five to seven, fewer only when the user asks for a smaller run. Three are fixed:

- **Inventory**: what the target does today, with locations, including what its documentation omits. For a concept for something new: what exists that the new thing builds on, touches or replaces.
- **Review**: an independent read for defects in robustness, security and correctness.
- **Outward**: how comparable products and prior art solve this, and what the official documentation of the platform in use says.

Choose the rest from what the decision needs: interface and wording, first run and setup, performance, structure of the code, data model, operations, accessibility, cost, or a larger alternative such as a rewrite or another platform.

Done when every lens has a question no other lens answers, and together they cover the decision. Tell the user the three lines, the lenses and the number of agents, since the number is the cost, then go on.

## 4. Run the lenses

Start one agent per lens, all at once, each with a fresh context. Where the harness has no subagents, take the lenses one after another, each from its brief alone. The brief carries:

1. the three lines and the baseline,
2. all lenses with their questions, and which one is this agent's,
3. the Read-only section above, verbatim,
4. the absolute path of [`LENS.md`](LENS.md), which the agent reads for what to return.

Done when every lens has returned every part `LENS.md` sets, and its *Covered* list reaches every part of the target its question touches. Ask a lens again when its list has holes, or a finding lacks its location or its consequence.

## 5. Check the claims

A **claim** is any statement of fact that the report will carry: a number, a behaviour, a location, an absence, a fact from outside. List every claim from the lenses, each with its location or source and without the reasoning behind it.

Hand the list to one fresh agent, the checker, with the three lines, the commit and the Read-only section. It tests each claim, against the code, by running it, or at the source that owns an outside fact, and answers per claim: **confirmed**, **wrong** with the correction, or **not checkable**, naming what the test would have needed (a device, an account, access, a step Read-only rules out).

Correct the wrong ones, and drop what rested on them. Done when every claim from the lenses has a verdict.

## 6. Write the report

Read [`REPORT.md`](REPORT.md) and write the page yourself: weighing the lenses against each other, the concepts and the order of the stages are the lead's work.

Done when every section `REPORT.md` requires is filled from the lenses and the checker, every stage can be ordered by its number, and the page has been opened, or read through where no browser is at hand, against REPORT.md's list for the page.

## 7. Hand over

Save the page as `overhaul-<target>-<date>.html` where the user says, otherwise in the user's Downloads folder, or untracked in the working directory where the harness may write nowhere else. Reply with its absolute path, the thesis, the stages as a numbered list and what is not verified. Then stop: building starts on the user's order.
