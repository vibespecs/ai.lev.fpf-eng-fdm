# FDM.4 - Establish What a Financial Action Changed {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Financial Domain Modeling Principles Framework* (2026-09-29), `Engineering DPF Suite/FINANCIAL-DOMAIN-MODELING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

**Type:** Architectural

## FDM.4:0 - Use this when {#use-this-when}

Use this pattern when someone says a financial action is complete but the resulting position is uncertain. Approval, a sent instruction, a system posting and settlement can support different claims.

The pattern governs an account of an actual action or event's financial effect. It returns a supported change, supported non-change or a specific unresolved effect, including the remaining position where that matters.

Use an adequate established effect account directly. Reconstructing an uncontested payment from every source adds no value when the receiving use already has sufficient evidence.

## FDM.4:1 - Problem frame {#problem-frame}

A lending decision can authorize a next step without funding a borrower. An agreement can create a duty before funding. A payment instruction can be accepted for processing while the recipient still lacks usable funds. A payment can discharge only part of an obligation.

The financial question concerns the effect that actually obtains under the applicable arrangement. Its answer needs both the relevant institutional or contractual rule and adequate evidence of the event that satisfies its conditions.

## FDM.4:2 - Problem {#problem}

A local completion label can be used to infer a wider result. That inference can leave a debt overstated, a payment falsely treated as available or a proposed agreement treated as effective.

The opposite error is to require physical cash movement for every financial change. Waiver, valid modification or another recognized act can change a position under its applicable rule. The method must recover the actual effect mechanism rather than select it from the action's label.

## FDM.4:3 - Forces {#forces}

Operational systems need timely completion signals. Their signals have scopes and can arrive before or after the effect relevant to another participant. Several dates may therefore be useful.

Evidence can disagree because of timing, identity or meaning as well as an actual failed action. Resolving the discrepancy requires enough context to distinguish those explanations, without turning every routine completion into a full investigation.

## FDM.4:4 - Solution {#solution}

### FDM.4:4.1 - Name the claimed change and prior position {#name-the-claimed-change-and-prior-position}

State what is supposed to have changed, for which party, under which arrangement and at what relevant time. Recover the prior position to the extent needed to explain the effect. FDM.1 supplies a missing position account; FDM.2 resolves an uncertain party boundary.

Distinguish a changed permission, duty, usable resource, recorded statement and business outcome. If a message says only “approved”, establish what its sender actually approved before treating it as evidence of another result.

### FDM.4:4.2 - Recover the rule that gives the event its effect {#recover-the-rule-that-gives-the-event-its-effect}

Obtain the applicable terms or institutional rule. Identify the event or action the rule recognizes, the actor and authority where required, the conditions and the effective time. Some effects require a communicative act; others depend on performance or another recognized occurrence.

[A.2.8][DUTY], [A.2.8.PER][PER] and [A.2.9][ACT] supply the respective duty, permission and communicative-work questions. Use the relevant specialist for disputed local terms. A record can be constitutive if the applicable rule gives the recording act that role.

### FDM.4:4.3 - Establish what actually occurred {#establish-what-actually-occurred}

Inspect the evidence relevant to that rule and effect. Match the parties, arrangement, amount and occurrence. Distinguish an instruction from its execution and a provider's local result from the recipient's result where those differences matter.

Retain the dates needed to interpret the action: occurrence, effective date, posting or actual availability can differ. Obtain only the dates that can change the present answer. Evidence sufficient for “instruction received” may be insufficient for “recipient can use the funds”.

If sources disagree, first compare their subjects, dates and meanings. Then investigate the remaining factual discrepancy. Do not select a source as decisive merely because its application is the most familiar one.

### FDM.4:4.4 - Derive the effect and remaining position {#derive-the-effect-and-remaining-position}

Apply the recovered rule to the established occurrence. State what changed and when. For a partial payment, use the applicable allocation rule to determine which amounts are satisfied and what remains. Preserve other interest, fees or conditions only where the actual arrangement requires them.

Keep the calculation answerable to that interpretation. If you can perform the arithmetic but cannot explain how it establishes the financial position, use [B.1.5.EW][EW] to locate the missing operation in the encompassing work. An unresolved contractual interpretation may need a qualified colleague's contribution; a computational correction addresses a different failure.

When the evidence establishes that the required event did not occur, return the supported non-change for that effect. When the rule or occurrence is unresolved, return the exact missing premise. An unresolved result is not proof of either performance or failure.

Relate the records to the resulting position. A necessary correction belongs in the appropriate account through its responsible process; do not silently rewrite history to make sources appear consistent. Use [ADM.4][ADM] when the participants' accounts require a broader comparison.

### FDM.4:4.5 - Return the result needed by the next user {#return-the-result-needed-by-the-next-user}

Supply the supported effect, time, remaining position and limits. Name the next responsible question when a rule, occurrence or correction still needs resolution.

FDM.3 uses the resulting state for later events. FDM.5 uses the effect when examining a participant's service result. A demonstrated financial change can be useful even when its longer-term benefit is not yet known.

## FDM.4:7 - Conformance Checklist {#conformance-checklist}

For the effect being asserted, examine whether:

1. The affected party, prior position, claimed change and relevant time are clear.
2. The applicable rule and its action, authority or occurrence conditions are established where required.
3. Evidence supports the actual event at the scope claimed.
4. The derived effect and any residual obligation follow the applicable terms.
5. Records, effective relations and resource availability remain distinct where their differences matter.
6. The result distinguishes supported change, supported non-change and unresolved effect.

A calculation can verify the consequence of supplied premises. It cannot establish the missing event or institutional rule.

## FDM.4:9 - Consequences {#consequences}

The practitioner can explain what a financial action actually changed and what remains. Local system success no longer automatically becomes a broader completion claim.

The work can expose a missing rule, uncertain event or account correction. Resolving it may require another participant or specialist.

## FDM.4:12 - Relations {#relations}

FDM.1–2 supply positions and parties. FDM.3 supplies contractual event logic and consumes the resulting actual state. FDM.5 uses the supported effect in a service-contribution account.

ADM.3, ADM.7–10 and the relevant financial practice supply effectivity, evidence, permission, usable provision and fulfillment questions at their own scope. A.2.8, A.2.8.PER and A.2.9 govern the underlying institutional distinctions.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root–3; applicable institutional rule and event evidence. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-fdm/contract/FDM-3#root @status:spec/done

#source spec://ai.lev/fpf-eng-fdm/source/FDM-4

[DUTY]: spec://ai.lev/fpf-spec/contract/A-2-8#root
[PER]: spec://ai.lev/fpf-spec/contract/A-2-8-PER#root
[ACT]: spec://ai.lev/fpf-spec/contract/A-2-9#root
[EW]: spec://ai.lev/fpf-spec/contract/B-1-5-EW#root
[ADM]: spec://ai.lev/fpf-eng-adm/pub/TOC#root
