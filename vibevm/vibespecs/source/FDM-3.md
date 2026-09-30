# FDM.3 - Derive Events and Conditional Flows from Financial Contract Terms: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## FDM.3:5 - Archetypal Grounding {#archetypal-grounding}

In the constructed loan, a lender advances 100 and the borrower owes one payment of 105 on day 30. Valid formation, currency and the fixed payment terms are supplied. The model can begin with:

| Event | Lender's cash flow under the stated schedule | Borrower's cash flow under the same schedule |
| --- | ---: | ---: |
| Successful advance | −100 | +100 |
| Contractual payment on day 30 | +105 | −105 |

The signs describe each party's perspective. The second row is contractual; actual receipt still requires performance.

For illustration, suppose a separate performance model assumes an 80% probability of payment of 105 and a 20% probability of payment of only 60, both on day 30. Its expected receipt is **0.8 × 105 + 0.2 × 60 = 96**. These probabilities are supplied assumptions, not an interpretation of an unexplained score. The expected amount is neither the contractual amount nor a discounted value.

If the actual payment is 60, retain that observation separately. Under the example's supplied application rule and absence of additional fees or interest, FDM.4 can establish 45 remaining due. The contractual schedule does not become “60 due” merely because only 60 was paid.

Now consider a conditional support arrangement for X. The terms require a payment of 80 only after a specified failure and valid demand. Its event model must preserve those conditions and the actual payment timing rule. It cannot supply 80 of unconditional day-7 funding merely because that amount appears in the document. If the rule does not establish when funds can arrive, the timing result remains unresolved.

## FDM.3:6 - Bias-Annotation {#bias-annotation}

A precise formula can attract more confidence than its inputs deserve. Keep the source and uncertainty of performance assumptions visible, especially when a score has been converted into a probability.

A familiar simple loan can also bias the interpretation of another instrument. Use its actual terms; a repeated software field name does not establish the same event behavior.

## FDM.3:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Using principal as the maturity payment.** Recover the amount's contractual meaning and derive the payment from the terms.

**Treating a schedule as a receipt forecast.** State the performance assumptions and retain the contractual obligation separately.

**Applying an undocumented default.** Establish whether the chosen convention belongs to the actual arrangement. If it is only a scenario assumption, say so where it changes the flow.

## FDM.3:10 - Architectural Rationale {#architectural-rationale}

Events and their conditions are central because an instrument's financial behavior depends on how the arrangement responds over time. A flat amount-and-date record can be sufficient for a simple fixed obligation; it needs extension when conditions alter that obligation.

Separating contractual behavior from performance keeps both interpretable. A single blended “forecast cash flow” can be useful to its intended decision, but its construction must retain the contractual and scenario meanings needed to explain or revise it.

## FDM.3:11 - SoTA-Echoing {#sota-echoing}

The practice question is how to turn financial terms into inspectable event behavior. The selected line adopts ACTUS's distinction between terms and the scheduled contractual events derived from them. It changes §§4.2–4.3 by making conditions, state and event consequences explicit. Actual use of a particular ACTUS contract type requires checking its specification and encoding.

At comparable first-case effort, deriving two qualified event rows is more useful than mapping an unexplained “loan amount” into a cash-flow field. An executable model is preferable when the relevant branching and repeated calculations justify its cost.

FDM.4 supplies the separate actual-effect question. Reopen the event model when terms, initial state, event ordering or a material scenario assumption changes.


## FDM.3:End {#end}
