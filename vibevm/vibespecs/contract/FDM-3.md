# FDM.3 - Derive Events and Conditional Flows from Financial Contract Terms {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

**Type:** Architectural

## FDM.3:0 - Use this when {#use-this-when}

Use this pattern when a financial instrument's amount or due-date field cannot answer what happens under its terms. The question may concern payment timing, a conditional draw, repayment, a guarantee or another event that changes the required flows.

The pattern governs an event and flow model of the relevant arrangement. It returns contractual events under stated terms, any scenarios needed for the question and their relation to observed performance.

Use an adequate existing schedule directly when its conditions match the question. A new diagram is unnecessary if the contractual behavior is already clear.

## FDM.3:1 - Problem frame {#problem-frame}

“Loan amount 100” does not say whether 100 is the advance, current principal or payment due. A repayment amount may depend on elapsed time, a reference value, an option or prior events. Its date may depend on a calendar rule rather than a number typed into a report.

Contractual behavior and actual performance also differ. An amount due can remain unpaid. A forecast of receipts requires assumptions about performance even when the contractual schedule is certain.

## FDM.3:2 - Problem {#problem}

A flat list of amounts and dates can conceal the conditions that produce them. Treating the resulting schedule as an unconditional cash forecast then imports an unsupported performance assumption.

A model of every possible contingency would be costly and often impossible. The working problem is to recover the contractual logic and the conditional outcomes that can change the present use.

## FDM.3:3 - Forces {#forces}

Contract terms can be precise while required inputs remain uncertain. An amount linked to a future reference value may be contractually well defined without being numerically known today.

Simplification is useful when it preserves the receiving answer. It becomes misleading when it erases an exercise condition, timing rule or priority of events that changes the amount or obligation.

## FDM.3:4 - Solution {#solution}

### FDM.3:4.1 - Recover the arrangement and intended question {#recover-the-arrangement-and-intended-question}

Identify the relevant parties, instrument or arrangement, version of the terms and time from which the model starts. Use FDM.1 or FDM.2 for missing positions or boundaries.

State the needed answer: the contractual schedule, an adverse funding scenario, the consequence of an option or another specific question. Reuse existing terms and schedules to the extent that their scope and assumptions match.

### FDM.3:4.2 - Extract the terms that determine the events {#extract-the-terms-that-determine-the-events}

Recover the event conditions and their consequences from the applicable arrangement. For each relevant event, establish who acts or pays, to whom, what amount or quantity is determined, in which currency and at what time. Include calculation, calendar, exercise, notice or settlement rules when they can change the answer.

Identify the state from which an event is evaluated. Outstanding principal, accrued amounts or a prior exercise can matter. Preserve the rule that updates this state after an event; an amount calculated from an outdated principal can be wrong even when its formula is correctly implemented.

Ask the responsible specialist about a missing or disputed term. A software default can represent an explicit modeling assumption, but it cannot silently establish the actual contract's meaning.

### FDM.3:4.3 - Derive and inspect contractual behavior {#derive-and-inspect-contractual-behavior}

Work through the relevant events in their applicable order. Apply the terms and state changes to derive the schedule or conditional branches. Keep terms, supplied input values and derived amounts distinguishable enough to inspect.

A simple fixed-payment loan can be modeled in two rows. An instrument with contingent payments may require branches or an executable model. Where an event's order or date can change the result, inspect that boundary case explicitly. Choose the representation from the behavior the question needs.

Check that the resulting flows agree with the terms under representative conditions. A calculation can be mechanically correct while using the wrong meaning for “amount”, the wrong party or an inappropriate initial state.

### FDM.3:4.4 - Add scenarios and performance without replacing the contract {#add-scenarios-and-performance-without-replacing-the-contract}

For a scenario, state the additional assumptions: market values, exercise, default, recovery or another condition relevant to the use. Derive the resulting conditional flows. If a probability or expectation is needed, obtain an adequate basis for it and retain its conditions.

Keep the contractual schedule available alongside expected or scenario flows. An expectation is an account across possible outcomes under a model; it is not another amount that every counterparty must pay. Likewise, an observed payment belongs to the actual-performance account. FDM.4 establishes its effect on remaining positions.

A financial choice or valuation may need discounting, risk treatment or comparison with alternatives. Supply the qualified flows to the relevant financial method; the event model alone does not select those decision rules.

### FDM.3:4.5 - Return the usable event model and its limits {#return-the-usable-event-model-and-its-limits}

Return the contractual or conditional flows, relevant parties, time rules and assumptions at the detail the receiving use needs. Name a missing term or uncertain input where it changes the answer.

Return a range, conditional branches or an unresolved amount when the available terms and inputs do not determine one value. Reopen the model when terms, relevant state, a relied-on scenario premise or the intended use changes.

## FDM.3:7 - Conformance Checklist {#conformance-checklist}

For the intended flow use, examine whether:

1. The arrangement, parties, relevant terms and initial state are identified.
2. Event conditions, amounts, currencies, timing and state updates follow the applicable terms or explicit assumptions.
3. The representation retains the branches and ordering that can change the answer.
4. Contractual, scenario, expected and actual flows remain distinguishable.
5. Missing terms and uncertain inputs are exposed where they affect the result.
6. A valuation or decision claim uses the further method and evidence it requires.

A generated schedule demonstrates the calculation under its inputs. It does not establish valid formation, future performance or financial suitability.

## FDM.3:9 - Consequences {#consequences}

The user can explain where an amount or date comes from and can compare contractual requirements with conditional and actual outcomes. The result can feed funding, risk, reporting or service work.

The model may reveal that a previously definite number depends on an unresolved term or uncertain input. That limits reliance while giving the recipient a precise next question. Greater instrument complexity increases construction and maintenance effort.

## FDM.3:12 - Relations {#relations}

FDM.1–2 supply adequate positions and party boundaries. FDM.4 establishes actual events and their effects; FDM.5 uses the flows relevant to a participant's service result.

SIE.3–6 supply general model construction and connection. [Management Accounting, MA.4][MA4] reconciles operating, reporting and cash accounts; [MA.5][MA5] uses the relevant conditional flows in its forecast. The responsible financial practice supplies any additional valuation or choice method.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root–2 for terms and parties; actual effects use spec://ai.lev/fpf-eng-fdm/contract/FDM-4#root. @status:spec/done

#source spec://ai.lev/fpf-eng-fdm/source/FDM-3

[MA4]: spec://ai.lev/fpf-eng-ma/contract/MA-4#root
[MA5]: spec://ai.lev/fpf-eng-ma/contract/MA-5#root
