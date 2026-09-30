# FDM.2 - Choose Party and Group Boundaries for Financial Modeling {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

**Type:** Architectural

## FDM.2:0 - Use this when {#use-this-when}

Use this pattern when a financial question crosses companies, accounts, funds or groups and the chosen boundary could change the answer. A founder's portfolio and a reporting group can include different entities; identify separately which party must make the payment.

The pattern governs the party and grouping account used for a financial question. It returns identified underlying parties and positions, a grouping criterion and the aggregation or support relations warranted for that use.

Use an adequate established boundary directly. A different display arrangement alone need not reopen an undisputed debtor or reporting subject.

## FDM.2:1 - Problem frame {#problem-frame}

One fund tracks investments by individual legal entity. Another groups startups associated with the same founders. Both views can support useful work, yet a shared founder does not automatically combine their obligations or accounts.

The question determines the relevant relation. Payment feasibility concerns the debtor's timely usable resources. A portfolio analysis can concern shared exposures without any support between entities. A reporting aggregate follows its applicable inclusion and elimination rules. The model must retain these differences while allowing the useful views to connect.

## FDM.2:2 - Problem {#problem}

A convenient group key is often used as if it settled control, liability, support and resource availability together. Adding the members' balances then conceals the very restriction that changes the financial answer.

Forcing every question into separate-entity accounts has a different cost: it can miss correlated exposure or an actual support arrangement. The practitioner needs the boundary warranted by this question, with enough underlying structure to prevent an aggregate from acquiring another meaning.

## FDM.2:3 - Forces {#forces}

An aggregate makes comparison manageable. Its simplicity is useful only while the omitted distinctions do not change the intended conclusion. The relevant membership and support conditions can also change over time.

Some relations establish a duty or power; others support a prediction of voluntary action. Both may matter, but treating an expectation as committed funding gives the prediction an unwarranted institutional effect.

## FDM.2:4 - Solution {#solution}

### FDM.2:4.1 - Start with the financial consequence being examined {#start-with-the-financial-consequence-being-examined}

State whose payment, position, exposure, control or report is at issue and the relevant time. Identify the actual entities and accounts involved before selecting a group label.

For a payment, find the party that bears the obligation. For a portfolio question, identify the investments or exposures being compared. For a required report, obtain the applicable reporting boundary from the responsible practice. Use [SIE.5][SIE] when the entities themselves or their continuity are disputed.

### FDM.2:4.2 - State why these members belong together {#state-why-these-members-belong-together}

State the question the grouping serves and its inclusion criterion. The criterion may concern a common founder, control, contractual support or inclusion in the consolidated accounts under the applicable reporting rule. Establish membership at the time relevant to that question. Preserve the underlying positions when a group view is produced.

Different criteria can produce overlapping groups. Keep them connected when the receiving use needs them. A single hierarchy need not carry every financial relation.

### FDM.2:4.3 - Recover what connects the positions {#recover-what-connects-the-positions}

For a proposed support or resource-availability conclusion, inspect the actual connecting relation. A guarantee, committed facility, permitted transfer, control relationship and expected voluntary payment answer different questions.

Establish the relevant parties, content, limits, conditions and timing. A guarantee can give the creditor a further conditional claim without placing cash in the primary debtor's account now. Permission to transfer does not establish a transfer obligation. A support commitment does not establish timely performance. Control can matter while restrictions still prevent a particular use of funds.

When support is merely expected, preserve it as a scenario assumption with the reason for that expectation. A risk account may reasonably consider it; an account of cash already available needs the stronger fact it claims.

### FDM.2:4.4 - Build the warranted aggregate {#build-the-warranted-aggregate}

Combine only amounts whose meaning, time, currency and inclusion rule are adequate for the receiving use. Preserve restrictions and conditional relations that can change the result. Apply the relevant reporting or specialist rule where valuation, conversion, netting or elimination is required; the group label does not supply those rules.

For a payment question, derive the debtor's usable funds at the payment time after other relevant receipts and obligations. For a risk question, retain the exposures and dependencies needed to understand adverse scenarios. Do not silently use the risk aggregate as the payment-feasibility balance.

### FDM.2:4.5 - Return the boundary and its financial meaning {#return-the-boundary-and-its-financial-meaning}

Return the relevant parties, membership rule, positions and justified aggregate or support conclusion. State what remains unresolved where it affects use: an entity identity, support condition, restriction, payment time or aggregation rule.

Use [SIE.6][SIE] to combine the relevant claims into a qualified answer once their financial meanings are established. Its result can retain several claims or report conflict, non-comparability or an unresolved premise. FDM.3 develops conditional support flows; FDM.4 establishes the effects of an actual transfer. A sufficient ordinary boundary can be used without constructing every other group view.

## FDM.2:7 - Conformance Checklist {#conformance-checklist}

For the boundary's stated use, examine whether:

1. The financial question, relevant time and underlying parties are clear.
2. Group membership follows an identified criterion adequate for that question.
3. Liability, control, support, permission and expected behavior remain distinct where their differences matter.
4. An aggregate retains the necessary time, currency, restrictions and applicable composition rule.
5. A claim of available funding has adequate support for timely usability, and unresolved premises remain visible.

A correct membership list establishes the group under its criterion. It does not establish every financial conclusion someone might draw from that group.

## FDM.2:9 - Consequences {#consequences}

The user can compare group views without erasing the party that bears an obligation or the conditions of support. This exposes both false funding comfort and overlooked shared exposure.

The model can require more than one structure. Maintaining those structures is justified by their uses; unused groupings add cost without improving the financial answer.

## FDM.2:12 - Relations {#relations}

FDM.1 supplies positions, FDM.3 their conditional flows and FDM.4 actual changes. FDM.5 uses the relevant participant boundary when examining a service result.

SIE.5 supplies unresolved identity work and SIE.6 composition. Use [C.32.MWA][MWA] when a financial-practice architecture question spans several structures, starting from representative performed work or a prospective use case. The relevant accounting, legal or financial practice supplies a disputed reporting, liability or aggregation rule.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root for positions; spec://ai.lev/fpf-eng-sie/contract/SIE-5#root–6 for identity and composition. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root @status:spec/done

#source spec://ai.lev/fpf-eng-fdm/source/FDM-2

[SIE]: spec://ai.lev/fpf-eng-sie/pub/TOC#root
[MWA]: spec://ai.lev/fpf-spec/contract/C-32-MWA#root
