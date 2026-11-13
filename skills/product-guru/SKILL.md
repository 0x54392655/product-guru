---
name: product-guru
description: Draft or edit product tickets, short product briefs, acceptance criteria, and product explanations in clear, precise English. Use for PM writing or requests to simplify product requirements. Applies STE-inspired clarity rules; does not verify ASD-STE100 conformance.
---

# Product Guru

Make product writing easy to understand and safe to act on. A reader should know what must change, why it matters, and what remains undecided.

Use the requested format and audience. Keep established team templates. For a small edit, return the edit; do not expand it into a full ticket or brief. These instructions govern product writing for the current task, not unrelated work.

## Preserve the meaning

- Keep every requirement, condition, exception, limit, unit, and explicit exclusion. Keep the strength of obligations: do not turn a suggestion into a requirement.
- Preserve identifiers, API fields, status names, numbers, quotations, and exact UI text. Simplify the explanation around them.
- Use one term for one concept. Follow the supplied glossary. Do not merge distinct concepts, such as a request timeout and a payment failure.
- Keep facts, proposals, and unknowns distinct. Do not invent research, metrics, deadlines, commitments, owners, legal requirements, or system behavior.
- In a rewrite, change the expression, not the product decision. In a drafting task, offer necessary suggestions as proposals until the user accepts them.

## Write so the reader can act

- Give each sentence one main point. Aim for 20 words or fewer. Split a longer sentence when this improves understanding. Preserve meaning and exact strings before meeting a word target.
- Name the actor and use a direct verb: "The service sends an email." If the actor is unknown, identify the gap instead of guessing.
- Put a condition before the result when it affects what the reader must do or expect: "If the upload fails, show the error message."
- Prefer familiar, concrete words. Replace vague phrases such as "enhance the experience" with the intended behavior, if the source gives it.
- Remove filler, repetition, metaphors, and unnecessary acronyms. Explain necessary domain terms for the intended audience.
- Use bullets for separate requirements or checks, and numbered steps for an ordered process. Keep paragraphs focused on one subject.
- Keep qualifications that affect decisions. Shorter text is not an improvement if it hides uncertainty or removes necessary detail.

## Resolve uncertainty without inventing scope

Use relevant context already provided or available in authorized sources. Do not search unrelated systems or change external tickets just to draft text.

If a missing fact prevents a useful draft, ask the smallest question that resolves it. Otherwise, draft the known parts and put material gaps under **Open questions**. Do not fill gaps with plausible defaults or turn unknown behavior into acceptance criteria.

If sources conflict, identify the conflicting requirements and request a decision. If the proposed outcome is too vague to specify, ask what observable change is wanted. Do not invent a feature to make the wording concrete.

## Choose the smallest useful artifact

**Ticket:** Use a concrete title, the problem or intended outcome, the required behavior, and acceptance criteria. Include open questions only when needed. Keep each criterion observable: name the relevant condition and expected result. Use Given/When/Then if requested or customary. Add failure cases only when supplied or necessary to make an agreed requirement unambiguous; mark other cases as questions or proposals. Include implementation details when requested or when they are actual constraints.

**Short product brief:** Explain the user and problem, evidence, intended outcome, proposed scope, and unresolved decisions. Include a measure of success when known. Label a suggested measure as a proposal. Avoid empty template sections and fabricated business cases.

**Explanation:** State the main idea first. Explain the mechanism in the order the reader needs. Use a concrete example when it helps; identify hypothetical examples. Keep relevant limits and uncertainty.

For examples of faithful rewrites and unresolved requirements, read [references/examples.md](references/examples.md) when useful.

## Check before returning

Compare the draft with the source. Restore any lost conditions or distinctions. Remove unsupported additions. Check that each agreed acceptance criterion can be verified without guessing what success means. Replace vague pronouns and inconsistent terms.

Return the requested artifact directly. Add questions or a short explanation only when they help the user make a decision. Do not attach a writing score or self-review checklist unless requested.

This is an independent, STE-inspired writing approach. It does not include the ASD-STE100 dictionary or verify conformance. If formal conformance is requested, explain that this skill cannot establish it and identify the need for a review against the official standard.
