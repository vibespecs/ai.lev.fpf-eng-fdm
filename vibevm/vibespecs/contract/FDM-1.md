# FDM.1 - Recover the Financial Position Behind a Record {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

**Type:** Architectural

## FDM.1:0 - Use this when {#use-this-when}

Use this pattern when someone relies on a balance, agreement, score or financial label without being able to say whose position it describes and under which terms. Begin with the party and the financial question the record is being used to answer.

The pattern governs an account of a financial position: the relevant right, obligation or other financial interest of an identified party under stated conditions and at a relevant time. It returns the warranted position and its relation to the records and resources involved.

Use an already adequate account directly. A cosmetic change to a report does not require recovering an undisputed position from the beginning.

## FDM.1:1 - Problem frame {#problem-frame}

Financial systems hold statements about parties and their positions. The word “claim” can refer either to an assertion in a report or to a creditor's right to receive something. Those meanings have different consequences. A report can assert that a lender has a right; the assertion and that right remain distinguishable.

Similarly, a loan agreement, a funded loan position, an account entry and the proceeds available to the borrower are connected without being the same subject. The receiving use determines which of these must be established.

## FDM.1:2 - Problem {#problem}

A record's label and amount can make its financial interpretation appear settled. If the party, terms or time are wrong, a correctly copied number can still answer the wrong question. Treating the record as the position also prevents the practitioner from explaining a stale entry, disputed obligation or valid agreement that has not yet been funded.

## FDM.1:3 - Forces {#forces}

A practitioner needs an answer quickly enough to support work. Reconstructing every institution and document is excessive when an adequate established account is available. Yet a material gap cannot be supplied merely by trusting a familiar field name.

The position can be clear while its future performance is uncertain. The model must retain that difference: a right to a future payment is not an assurance that the payment will occur.

## FDM.1:4 - Solution {#solution}

### FDM.1:4.1 - State the financial question and relevant party {#state-the-financial-question-and-relevant-party}

Ask what someone intends to conclude from the record: who owes, who may receive, who bears a loss, what is available or another specific result. Identify the actual party whose position matters and the counterparty or other participant required to interpret it.

Resolve a material identity or grouping uncertainty through FDM.2 or [SIE.5][SIE]. A common trading name, group identifier or database key can help locate the party but cannot settle a disputed entity boundary.

### FDM.1:4.2 - Recover the position from its applicable basis {#recover-the-position-from-its-applicable-basis}

Obtain the terms and institutional basis adequate for this question. Establish what right, duty or financial interest they provide, to whom, against whom where relevant, with what content, conditions and time. Use competent interpretation when an actual rule or term is unresolved.

A document can provide evidence and, under an applicable rule, its execution or another recognized act may help institute a relation. Recover that rule and event when they matter. Do not infer the existence or absence of an obligation solely from whether a database entry is present.

[A.2.8][DUTY] supplies the question whether an individual duty actually obtains. A permission uses [A.2.8.PER][PER].

### FDM.1:4.3 - Relate descriptions and resources to the position {#relate-descriptions-and-resources-to-the-position}

Identify what each source describes, the time it concerns and any limitation affecting reliance. A contract description, a servicing record and a customer's statement can refer to the same loan while differing in date, purpose or evidential support.

Distinguish the position from resources actually available. A borrower can owe repayment while proceeds have already been spent. A lender can have a funded right to payment while the borrower cannot currently pay. A displayed balance can be evidence about these facts, but its interpretation still needs the relevant account and availability conditions.

Retain a prospective position as prospective. A score or offer can inform a decision without establishing an agreement. Conversely, applicable terms can establish duties at valid formation before disbursement. Examine the actual conditions rather than imposing one universal sequence.

### FDM.1:4.4 - Return what is warranted for this use {#return-what-is-warranted-for-this-use}

Return the party, financial relation, content, conditions and time at enough detail to answer the question. Relate the material records to that account and name any discrepancy or missing premise.

Use FDM.3 when the receiving question needs the event and flow consequences. Use FDM.4 when an actual action may have changed the position. If the position is already sufficient for a routine report or decision, supply it without expanding the model.

## FDM.1:7 - Conformance Checklist {#conformance-checklist}

For the proposed interpretation, examine whether:

1. The actual party and financial question are identifiable.
2. The right, obligation or other interest has an adequate basis, content, conditions and time.
3. Assertions and records about the position remain distinguishable from the position itself.
4. Actual resources and expected future performance are not inferred from a position alone.
5. The result supplies an adequate answer or names the particular identity, term, rule or evidence still missing.

An adequate description supports its stated interpretation. Its existence alone does not prove formation, funding or performance.

## FDM.1:9 - Consequences {#consequences}

The recipient can use an amount with its financial meaning and can distinguish uncertainty about a position from uncertainty about payment. The model also makes a disagreement between records intelligible.

The cost is recovering material terms and relations that a label had concealed. Adequate existing accounts reduce that cost; unresolved institutional interpretation limits the conclusion the model can supply.

## FDM.1:12 - Relations {#relations}

FDM.2 resolves the party or group boundary; FDM.3 derives contractual behavior; FDM.4 establishes actual changes. FDM.5 uses an adequate position model when tracing a service's contribution.

A.2.8 governs the individual-duty question, A.2.8.PER the permission question and A.2.9 communicative work where its occurrence matters. [ADM.2–4][ADM] supply the corresponding administrative participant, effectivity and account questions. SIE supplies general identity and correspondence methods without replacing the financial terms.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-spec/contract/A-2-8#root and spec://ai.lev/fpf-spec/contract/A-2-8-PER#root; spec://ai.lev/fpf-eng-fdm/contract/FDM-2#root for a disputed party. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-fdm/contract/FDM-2#root, spec://ai.lev/fpf-eng-fdm/contract/FDM-3#root, spec://ai.lev/fpf-eng-fdm/contract/FDM-4#root, spec://ai.lev/fpf-eng-fdm/contract/FDM-5#root @status:spec/done

#source spec://ai.lev/fpf-eng-fdm/source/FDM-1

[SIE]: spec://ai.lev/fpf-eng-sie/pub/TOC#root
[DUTY]: spec://ai.lev/fpf-spec/contract/A-2-8#root
[PER]: spec://ai.lev/fpf-spec/contract/A-2-8-PER#root
[ADM]: spec://ai.lev/fpf-eng-adm/pub/TOC#root
