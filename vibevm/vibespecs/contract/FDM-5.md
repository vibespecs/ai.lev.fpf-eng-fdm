# FDM.5 - Trace a Financial Service to a Participant's Result {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

**Type:** Architectural

## FDM.5:0 - Use this when {#use-this-when}

Use this pattern when a score, report, advice, interface or transaction service is called a financial benefit without explaining the receiving use. Begin with the participant and the result the service is supposed to help them obtain.

The pattern governs an explanation of a financial service's contribution. It returns the relevant output, use, financial effect and participant result, with the support and uncertainty appropriate to the claim being made.

Use an adequate existing contribution account directly. A routine service need not be redesigned merely to describe its established result.

## FDM.5:1 - Problem frame {#problem-frame}

A scoring team can improve predictive accuracy while leaving lending decisions unchanged. An admission tool can produce accurate client information while a separate arrangement determines permission to use a service. A payment provider can complete its own processing while the recipient still lacks usable funds.

Each output can be useful. Its contribution depends on a receiving participant, an actual or proposed use and the financial result that use can affect. The tool developer, decision maker, service provider and beneficiary need not be the same participant.

## FDM.5:2 - Problem {#problem}

Output quality is often used as evidence of an entire financial result. This hides an unused output, missing decision, failed provision or adverse consequence for another participant.

Expanding the service boundary to every eventual business outcome is also unhelpful. It can make a provider responsible for results it neither decides nor supplies. The working problem is to explain the relevant contribution and its limits at enough scope to support the current decision.

## FDM.5:3 - Forces {#forces}

A service needs a recognizable useful result. Different participants can want different results, and a throughput measure may not express their shared interest. A legitimate refusal can be preferable to another admission.

Longer-term outcomes depend on more conditions than the service controls. A useful model can name those conditions without claiming either sole causation or complete ignorance about the service's contribution.

## FDM.5:4 - Solution {#solution}

### FDM.5:4.1 - Name the participant and intended result {#name-the-participant-and-intended-result}

Identify the participant whose result is at issue and what would improve for them: access to usable funds, a warranted lending decision, timely payment, a better understood exposure or another concrete gain. Establish the horizon and comparison the present question needs.

When several participants matter, retain their differing objectives and consequences. A lender's result and a borrower's result need not be identical. Use the responsible financial or management practice to settle a disputed objective or choice criterion.

### FDM.5:4.2 - Locate the output and its actual receiver {#locate-the-output-and-its-actual-receiver}

Identify the service output and who uses it. Separate the method, its implementation, one performed use and the produced result where their differences affect the account. A score is one output of a scoring arrangement; it is not the arrangement itself.

Ask the receiving participant how the output enters their work. A human or an authorized automated arrangement can use it. There is no mandatory intermediate change in a human's private expectation. Conversely, delivering data to an application does not establish that it influenced the relevant action.

A supplier can properly deliver information to another actor. Give that supplier's contribution its actual scope instead of redefining every upstream tool as if it directly provided the final financial outcome.

### FDM.5:4.3 - Follow the use through the financial effect {#follow-the-use-through-the-financial-effect}

Identify the decision or action the output can change and the financial relation or resource consequence that action can establish. Use FDM.1–4 where the position, terms or actual effect is unclear.

For a proposed service, explain the mechanism and assumptions under which the contribution is expected. For an actual service, obtain evidence of the receiving use and effect at the scope claimed. These can have different truth status within the same explanation.

Follow the connection far enough to answer the participant's question. A loan can provide usable proceeds; an equipment purchase can fail to deliver a working asset; changed demand can defeat the expected return from that asset. The financial service can have supplied its promised result while a later business outcome fails.

### FDM.5:4.4 - Examine the contribution and its failure points {#examine-the-contribution-and-its-failure-points}

Ask what would happen without this output or with the relevant alternative. Is the decision unchanged? Does another source already supply the same information? Can funding, authority, timing, delivery or subsequent use defeat the proposed gain?

Inspect the explanations that can change the present conclusion. A claim about improved financial outcomes may need a suitable comparison, uncertainty account and evidence of causes. An output-accuracy measure alone cannot supply them. Use the relevant evaluation or inquiry method when that further claim is required.

Preserve justified narrower claims. The service may improve the available decision information while its outcome effect remains unmeasured. It may supply a usable financial result under conditions outside its control. Locate the unanswered question rather than collapsing all evidence into either “benefit proved” or “no value”.

### FDM.5:4.5 - Return a qualified contribution and next action {#return-a-qualified-contribution-and-next-action}

Return an explanation that a receiver can use: the participant, service output, receiving use, relevant financial effect, intended result and material conditions. A simple connected paragraph can be enough.

State the supported result and the next missing evidence or decision. A contribution model can be complete for its current use before the loan matures or a long-term causal study finishes. A wider promise requires the further evidence appropriate to that promise.

## FDM.5:7 - Conformance Checklist {#conformance-checklist}

For the contribution being claimed, examine whether:

1. The relevant participant, intended result and horizon are identifiable.
2. The service output and receiving use have adequate meanings and boundaries.
3. The proposed or actual financial effect is connected through the applicable decision, action and terms.
4. Output quality, actual use, financial effect and later participant outcome retain their different evidence and uncertainty.
5. Material alternatives and failure points have been examined where they can change the conclusion.
6. The result states the supported contribution and any specific next evidence or decision needed.

A coherent contribution model supports understanding and inquiry. An observed improvement or causal benefit needs the evidence its stronger claim requires.

## FDM.5:9 - Consequences {#consequences}

The team can explain what its financial service contributes and can locate an unused output or failed connection. This can change the next investigation, service boundary or improvement effort.

The account may support a narrower benefit than a sponsor initially claimed. It can also reveal a useful contribution that a final-outcome-only measure concealed. A wider causal conclusion increases the evidence and comparison burden.

## FDM.5:12 - Relations {#relations}

FDM.1–4 supply the financial positions, boundaries, events and actual effects needed by this service question. [ADM.7–10][ADM] supply evidence, permission, usable provision and fulfillment where those administrative questions arise.

SIE supplies the general model connection. The relevant financial, operating or management practice supplies decision criteria and comparisons. When service design or provider choice is the unresolved task, use the relevant service-design or provider-selection method.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root–4 when financial meaning or effect is missing; relevant decision practice. @status:spec/done

#source spec://ai.lev/fpf-eng-fdm/source/FDM-5

[ADM]: spec://ai.lev/fpf-eng-adm/pub/TOC#root
