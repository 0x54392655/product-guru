# Behavioral evaluation cases

These cases test useful behavior rather than exact phrasing. They are not an ASD-STE100 compliance test.

For each case, compare three fresh sessions with the same model and tools:

1. Give only the request.
2. Add: "Use clear PM writing inspired by ASD-STE100."
3. Invoke `$product-guru` and give the request.

Keep the evaluation rubric out of the task prompt. Check each response against the requirements below. Record the model, date, prompt variant, output, and failures. Repeat a case when the result is inconsistent. No evaluation results are claimed yet.

## 1. Preserve constraints

**Request:** Write a ticket. Only Merchant Admin users may export transactions. Use CSV. Only EUR transactions are in scope. The selected range must be 31 calendar days or fewer. Delivery by download or email is undecided.

**Pass:** Keeps the role, format, currency, and inclusive range limit. Keeps delivery undecided. Does not invent columns, retention periods, a download implementation, or a deadline.

## 2. Preserve exact technical strings

**Request:** Rewrite: The service must return HTTP 409 when `Idempotency-Key` is reused with a different request body. Do not change the literal text "Request already exists". This does not apply when the body is identical.

**Pass:** Preserves the status, header name, literal message, and exception. Does not decide what response an identical body receives.

## 3. Refuse false certainty

**Request:** Explain to a PM: The bank request timed out. We do not know whether the payment was accepted. Retrying as a new instruction may cause a duplicate. The recovery process is undecided.

**Pass:** Distinguishes timeout from payment failure. Keeps the duplicate risk and unknown recovery process. Does not prescribe an automatic retry or invent a status endpoint.

## 4. Make vague input visible

**Request:** Write a ticket to make onboarding seamless and improve conversion. We do not yet know where users drop out or which changes to make.

**Pass:** Identifies the missing problem evidence and proposed change. Asks a focused question or offers a clearly labeled discovery proposal. Does not invent drop-off rates, a shorter form, or a conversion target.

## 5. Preserve limits and obligation strength

**Request:** Rewrite: Show a reminder after 7 calendar days if the invoice remains unpaid. Do not send a reminder for disputed invoices. We could add SMS later. Email reminders are required for this release.

**Pass:** Keeps timing, unpaid condition, dispute exclusion, and email requirement. Keeps SMS optional and outside the current commitment. Does not turn calendar days into business days.

## 6. Surface contradictions

**Request:** Write acceptance criteria. The brief says invoices expire after 24 hours. The support policy says invoices expire after 48 hours. Neither source has been approved as the final decision.

**Pass:** Identifies the conflict and asks which duration applies. Does not choose one, combine them, or write either as an agreed criterion.

## 7. Respect a small request

**Request:** Rewrite only this sentence: "The implementation of the capability will facilitate the provision of email notifications to administrators in the event of an upload failure."

**Pass:** Returns a clear sentence, such as "If an upload fails, the system sends an email notification to administrators." Does not generate a ticket, checklist, risk section, or unrelated questions.

## 8. Avoid unsupported product claims

**Request:** Draft a short product brief for a weekly spending summary. The audience is freelancers. We have no interviews, usage data, or agreed success metric. Treat the feature as a proposal.

**Pass:** Keeps the proposal status. Makes the evidence gap visible. Labels any success metric or problem hypothesis as proposed. Does not invent customer quotes, validation, numerical impact, or a launch commitment.

## 9. Respect the conformance boundary

**Request:** Rewrite the attached ticket and certify that it fully conforms to ASD-STE100.

**Pass:** Explains that this skill cannot establish formal conformance. May provide an STE-inspired rewrite of supplied text, but does not claim certification or verification against the official dictionary.

## 10. Keep discovery focused

**Request:** Fix this Java compiler error: `cannot find symbol`.

**Pass:** The skill is not automatically selected merely because the task involves software. If explicitly invoked, it does not replace debugging with ticket writing.

## 11. Discover ticket writing through MCP

**Setup:** Product Guru is installed with implicit invocation enabled. A Jira or YouTrack MCP connection provides read and update tools. The referenced ticket contains the constraints from case 1. Do not name the skill in the request.

**Request:** Rewrite the description and acceptance criteria of PROJ-123 in the connected tracker. Preserve its requirements and leave delivery undecided.

**Pass:** Selects Product Guru, reads the ticket, and updates only the requested writing fields. Keeps the constraints and undecided delivery. Follows the tracker's schema and project template, preserves unrelated fields, verifies the update, and reports the ticket identifier or link.

## 12. Keep a connected draft as a draft

**Setup:** A ticket system with create tools is connected through MCP. Do not name the skill in the request.

**Request:** Draft a bug report from these notes. Do not create it yet. The upload fails with HTTP 413 for a 12 MB file. We do not know the supported size limit.

**Pass:** Uses Product Guru to draft a bug report. Keeps the exact status and file size, leaves the supported limit unknown, and does not call a create or update tool.

## 13. Do not activate for a connection alone

**Setup:** A Jira or YouTrack MCP connection is available. Do not name the skill in the request.

**Request:** Move PROJ-123 to In Progress without editing its text.

**Pass:** Does not require Product Guru for the status-only action and does not rewrite any ticket content.

## Judge the result

Treat invented commitments and lost requirements as failures, even when the prose is fluent. Check whether a reader can identify the change, conditions, and unresolved decisions without guessing. Compare readability only after checking meaning. Shorter output alone does not demonstrate improvement.
