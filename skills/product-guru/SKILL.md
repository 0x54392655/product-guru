---
name: product-guru
description: Write, rewrite, or refine tickets, issues, bug reports, user stories, acceptance criteria, and explanatory ticket comments. Use for ticket writing in chat or through Jira, YouTrack, Linear, GitHub Issues, or any ticket system connected via MCP, even when the skill is not named. Also use for short product briefs and product explanations. Does not apply to ticket lookup, status-only updates, or implementing a ticket.
---

# Product Guru

Make product writing easy to understand and safe to act on. A reader should know what must change, why it matters, and what remains undecided.

Use the requested format and audience. Keep established team templates. For a small edit, return the edit; do not expand it into a full ticket or brief. These instructions govern product writing for the current task, not unrelated work.

## Work with connected ticket systems

Apply the same writing rules when drafting or editing ticket content through any connected ticket system. The provider and tool names do not change the writing workflow.

When revising a referenced ticket, read its current content and relevant linked context through the available tools. Follow the project's templates, terminology, and field conventions. Use the actual tool schemas; do not assume that every tracker has the same fields or formatting.

For a draft request, return the draft. When the user asks to create or update a ticket, use the connected tools within that authorization. Change only the requested content and preserve unrelated fields such as status, assignee, priority, and sprint. Check the returned ticket or fetch it again to verify the change, and report its identifier or link. If the tools cannot write tickets, provide the prepared text and explain the limitation.

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

## Write for a reader who never saw the earlier design

Describe the current problem, intended behavior, interfaces and ownership so the ticket stands on its own. A ticket is an implementation brief, not a record of the conversation that produced it.

When a design changes, rewrite the affected sections in place. Remove discarded proposals, obsolete type/field names, resolved questions and comparisons that require knowledge of an abandoned design. Do not append correction paragraphs while leaving conflicting instructions elsewhere in the ticket. Explain the current concept and its purpose directly.

Review the whole ticket, including headings, acceptance criteria, dependencies and links. Replace links that present an abandoned design as the implementation reference. Consolidate repeated handoff or revision notes into one current statement. Keep implementation/publication evidence concise and relevant to the current handoff.

Preserve compatibility, migration, security and release requirements that still apply to real systems. Distinguish those operational requirements from an unimplemented proposal. Use ticket history for discarded design discussion unless the user explicitly requests a decision log or a historical comparison.

## Maintain an existing ticket set

When asked to align an epic or related tickets after a design change:

- Discover the complete requested set, including paginated child issues, and read each ticket's current content before editing. Check the current contracts and ownership where the change crosses ticket boundaries.
- Rewrite affected sections in place so each ticket has one coherent description of the current work. Remove discarded concepts, resolved questions, repeated revision notes and stale implementation references. Keep shared delivery evidence in the owning ticket and link to it from consumers.
- Check the responsibilities, acceptance criteria and dependencies together. Component tickets should be independently verifiable at their agreed boundary; put connected acceptance tests in the ticket that owns the integration. Preserve the agreed scope and delivery order.
- Leave unaffected tickets unchanged. Preserve status, assignee, priority, release information and other unrelated fields unless the user requests a change.
- Verify saved content and check the set again for inconsistent instructions. Report which tickets were reviewed and changed, plus any concrete unresolved issue. Do not treat a phrase search alone as proof that the tickets are understandable.

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

Compare the draft with the source. Restore any lost conditions or distinctions. Remove unsupported additions. Check that each agreed acceptance criterion can be verified without guessing what success means. Replace vague pronouns and inconsistent terms. Read the result as a new implementer: remove unexplained references to discarded designs and check that all sections describe the same current behavior.

Return the requested artifact directly. Add questions or a short explanation only when they help the user make a decision. Do not attach a writing score or self-review checklist unless requested.

This is an independent, STE-inspired writing approach. It does not include the ASD-STE100 dictionary or verify conformance. If formal conformance is requested, explain that this skill cannot establish it and identify the need for a review against the official standard.
