# FDM.1 - Recover the Financial Position Behind a Record: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## FDM.1:5 - Archetypal Grounding {#archetypal-grounding}

A lender considers advancing 100 to a borrower. In this constructed arrangement, valid formation, currency and the applicable terms are supplied: successful funding creates the stated funded position, with 105 contractually due on day 30. The model distinguishes the lender and borrower, their respective right and duty, and the proceeds made available on funding.

An earlier score of 0.72 is a produced assertion under its scoring method. Its scale and meaning must be known before it is interpreted even as a probability. The score alone establishes neither a lending decision nor the borrower's repayment obligation.

Suppose the signed arrangement also obliges the lender, before funding, to advance the amount once a specified condition is met. That supplied term gives the practitioner a separate pre-funding duty to examine. Waiting for disbursement before recognizing every obligation would lose it. If the actual formation or term is disputed, the model returns that exact uncertainty.

Now assume that the advance of 100 has occurred and the resulting obligation to pay 105 is established. After an adequately established payment of 60, the original agreement still describes the contractual payment of 105. FDM.4 can establish the remaining 45 under the example's application rule and absence of further fees or interest. A servicing record that still shows an unpaid 105 is now a discrepancy to investigate, not proof that the payment had no effect.

## FDM.1:6 - Bias-Annotation {#bias-annotation}

System designers may prefer facts represented in their own application; a contract specialist may emphasize the agreement while overlooking settlement or usable resources. Compare the accounts around the receiving financial question.

The loan is a debt example. Other financial interests require their actual relation and governing terms; do not force an ownership interest or conditional instrument into a simple lender–borrower account merely because that example is familiar.

## FDM.1:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Treating “claim” as one unambiguous object.** State whether the sentence concerns an assertion or a creditor's right. Then relate them where the report is evidence about the right.

**Making the database constitutive by default.** Establish what rule, if any, gives the relevant recording act that effect. A stale or missing entry otherwise remains a recording question.

**Deferring every duty until funds move.** Inspect the actual formation and conditional-performance terms. A valid unfunded arrangement can already have consequences.

## FDM.1:10 - Architectural Rationale {#architectural-rationale}

The financial position is the central subject because it is what the record is commonly used to infer. Beginning with the receiving question limits the reconstruction to distinctions that matter.

A dictionary-only account is sufficient when the issue is a shared term and the actual position is already known. It is inadequate when an individual party's right or duty remains unsettled. Starting instead with the complete financial-service chain can impose unnecessary work on a narrow position question.

## FDM.1:11 - SoTA-Echoing {#sota-echoing}

The practice question is how to give a financial record a warranted interpretation. The method uses FPF's distinction between an actual institutional relation and claims about it to interpret financial records. This changes §§4.2–4.3: establish the applicable relation and then connect the descriptions and resources.

FIBO is useful for financial concepts and relations that a local label obscures. It supplies reusable meaning rather than evidence that this particular party has this particular right. At the effort of clarifying one disputed label, a position account can expose a missing formation or time premise that a field renaming would retain.

Reopen the interpretation when actual terms, party identity or event evidence changes the position being described.


## FDM.1:End {#end}
