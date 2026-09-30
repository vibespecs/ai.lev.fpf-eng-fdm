# FDM.4 - Establish What a Financial Action Changed: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## FDM.4:5 - Archetypal Grounding {#archetypal-grounding}

### FDM.4:5.1 - A payment, an instruction and a modification {#a-payment-an-instruction-and-a-modification}

In the constructed loan, 105 is due on day 30. Adequate evidence establishes a payment of 60 by the borrower to the lender. The supplied application rule applies all 60 to that due amount; there are no additional fees or interest. The resulting unpaid amount is **45**.

A servicing report still showing 105 unpaid disagrees with that established effect. The model returns the 45 position and the report discrepancy. It retains the original 105 contractual schedule and the actual 60 payment as distinct statements, rather than editing either into the other.

Now suppose the available evidence instead establishes only that the borrower sent a payment instruction for 60. The evidence does not yet establish the event that the supplied terms recognize as payment. The claimed reduction to 45 remains unresolved. The next question is whether that event occurred, not whether subtraction was performed correctly.

A separate pre-funding example has different effect conditions. A valid modification, made by the competent parties under supplied terms, changes a lender's conditional advance obligation before any money moves. The model follows that rule and its actual occurrence. It does not wait for disbursement to recognize every change.

These examples demonstrate reasoning under their supplied premises. Another instrument's payment-allocation, formation or modification rule can produce a different result.

### FDM.4:5.2 - Deriving the position through an interpreted calculation {#deriving-the-position-through-an-interpreted-calculation}

Consider a variant in which receipt of 60 is established, but the supplied terms classify it as refundable cash collateral. The terms leave the borrower's loan obligation of 105 unchanged. Subtracting 60 from 105 still produces 45 arithmetically, but does not describe the remaining loan obligation under these terms. The account instead retains the obligation of **105** and the separate collateral position.

While applying the contractual classification, the modeler is deriving the financial effect and constructing the position account. What the larger account must explain determines what the local calculation may claim. The earlier repayment example permits the subtraction; this collateral example does not. The banking receipt supplies an occurrence to interpret, rather than becoming part of the modeler's act of interpretation.

Someone who can calculate but cannot interpret the collateral terms needs to learn to interpret them or obtain an adequate interpretation from an appropriate specialist. Once the interpretation is adequate, the account can proceed without a fresh investigation of the already established receipt. If the terms later provide that collateral is applied to the debt, establish the event and effect under that changed condition before updating the obligation.

## FDM.4:6 - Bias-Annotation {#bias-annotation}

A service team may equate its own successful step with the recipient's result. A financial reporter may give the latest posting more authority than its evidential meaning supports. Recover the effect and its rule before judging either account.

When the available sources cannot establish whether the event occurred, retain that uncertainty.

## FDM.4:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Closing the obligation from a sent instruction.** Establish the event the applicable arrangement recognizes as performance.

**Treating all postings as either constitutive or merely descriptive.** Recover the actual rule and the role of the recording act in that arrangement.

**Using one date for every consequence.** Retain distinct occurrence, effect or availability dates when they change the receiving answer.

## FDM.4:10 - Architectural Rationale {#architectural-rationale}

The method joins a governing rule with an actual occurrence because neither alone establishes the particular effect. A generic term describes what would happen; an event description becomes financially meaningful through the applicable conditions.

A transaction log is sufficient when it already supplies adequate evidence for a settled effect rule. A broad business-outcome inquiry is unnecessary for a narrow residual-balance question. The wider inquiry becomes useful when someone claims the financial change itself established the participant's benefit.

## FDM.4:11 - SoTA-Echoing {#sota-echoing}

The practice question is how to distinguish an actual financial effect from a decision, message or record. The method applies FPF's duty, permission and communicative-work distinctions to financial actions, with ADM.3 and ADM.9–10 supplying effectivity, usable provision and fulfillment questions.

This changes §§4.2–4.4: recover the effect rule, establish the occurrence and derive the remaining position. At the effort of examining one completion claim, it can distinguish “60 instructed” from “60 paid”, which a status-only reading conflates. More extensive investigation is justified when the unresolved premise changes the receiving use.

Actual local rules and event evidence govern an actual result. Reopen the account when either changes or when a later use requires a broader effect claim.


## FDM.4:End {#end}
