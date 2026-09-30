# FDM.2 - Choose Party and Group Boundaries for Financial Modeling: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## FDM.2:5 - Archetypal Grounding {#archetypal-grounding}

X must pay 100 on day 7. Its unrestricted cash available on that date, after all other receipts and obligations but before this payment, is 20. Y holds 150 in its own account. They share a founder. These are supplied facts of a constructed case.

The founder-group view can show both members and their balances. It does not settle X's ability to pay. X has an **80 shortfall** under the stated cash premise.

Suppose a duly established support arrangement requires Y to transfer 80 to X, with conditions that make it due before day 7. The model now contains a support obligation whose timely performance could close the gap. Until adequate evidence establishes the transfer or another means of timely availability, “support committed” remains different from “funds available”.

If the arrangement instead provides only a guarantee exercisable after X fails to pay, the creditor may have a further route under those supplied terms. X still lacks day-7 cash in the facts given. FDM.3 models the guarantee's actual trigger and timing; the model must not describe it as an earlier transfer.

If Y has no support commitment but the founder is expected to arrange a voluntary transfer, keep that event in the scenario that assumes it. For a portfolio-risk question, common dependence on that founder or on the same market can justify examining the members together even when no transfer is possible.

## FDM.2:6 - Bias-Annotation {#bias-annotation}

An investor may view a founder group as one economic story; a reporting system may prefer one legal identifier. Test both against the actual consequence being claimed.

Evidence of past voluntary support can inform an expectation. It does not by itself establish a present obligation or remove the possibility that support will arrive too late.

## FDM.2:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Funding X by summing X and Y.** Recover the relation and event that make Y's resources usable for X's payment.

**Reading a guarantee as cash in advance.** Use the actual trigger, beneficiary and payment conditions. The guarantee may answer a recovery question while leaving the immediate funding question open.

**Rejecting a useful risk group because its members are separate debtors.** Keep the debtor accounts and model the shared exposure for the risk use that needs it.

## FDM.2:10 - Architectural Rationale {#architectural-rationale}

The method begins with the consequence because there is no single group boundary that settles every financial question. It retains underlying positions so that aggregation can be interpreted and revised.

A single reporting tree is adequate when its rule and the receiving use match. Separate-entity accounts suffice for an isolated debtor question. Several connected views become useful when support, exposure and reporting differ. Their connection uses SIE's existing identity and composition methods, with the financial relations supplied here.

## FDM.2:11 - SoTA-Echoing {#sota-echoing}

The practice question is which party and group account makes a financial consequence intelligible. For financial groupings, the method adapts C.32.MWA's idea that several useful structures need not coincide. SIE.5–6 supply identity and composition methods.

This changes §§4.1–4.4: choose the boundary by the consequence, retain the members' positions and examine support separately. At the effort of naming the debtor and the support relation, it can expose a payment shortfall that a founder-group total hides. A larger organizational model is useful only when another material relation needs it.

The X–Y example demonstrates the difference between grouping entities and establishing support under its supplied conditions. Reopen the boundary when actual membership, support terms, restrictions or the receiving financial question changes.


## FDM.2:End {#end}
