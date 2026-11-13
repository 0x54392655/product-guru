# Examples

These examples illustrate this skill's own PM writing rules. They are not examples of verified ASD-STE100 conformance.

## Rewrite a ticket without adding requirements

### Input

Rewrite as a ticket. Merchants currently contact support to obtain transaction exports. We should enable users with the Merchant Admin role to independently facilitate the generation of CSV exports from the Transactions page, based on the selected date range. This is required for EUR transactions only. The permitted range must not exceed 31 calendar days. Non-admin users must not be able to export. The team has not decided whether the export is downloaded immediately or delivered by email.

### Output

**Title:** Let Merchant Admin users export EUR transactions

**Problem**

Merchants must contact support to get transaction exports.

**Required behavior**

Let users with the Merchant Admin role export EUR transactions from the Transactions page. Use the selected date range. Allow a maximum range of 31 calendar days.

**Acceptance criteria**

- A user with the Merchant Admin role can request a CSV export for a date range of 31 calendar days or fewer.
- The export contains EUR transactions within the selected date range.
- The export does not contain transactions in other currencies.
- An export cannot cover more than 31 calendar days.
- A user without the Merchant Admin role cannot export transactions.

**Open questions**

- Should the user download the export immediately or receive it by email?
- Which transaction fields must the CSV contain?
- How should the date range handle time zones and the start and end dates?

### Why this works

The rewrite keeps the role restriction, currency restriction, format, page, and range limit. It leaves delivery and data details undecided. It adds no background job, storage provider, response-time target, or delivery commitment.

## Keep uncertainty visible

### Input

Explain this to a product manager: A timeout at the bank interface does not definitively indicate payment failure. We may not yet know whether the bank accepted the payment. Retrying the payment as a new instruction could result in duplicate execution. We have not agreed the recovery process.

### Output

A timeout means we did not receive a response in time. The bank may still have accepted the payment.

If we send a new payment instruction, the bank could execute both instructions. The customer could pay twice.

We need to agree how to find the payment's status and when a retry is safe.

### Why this works

The explanation keeps the difference between an unknown result and a failed payment. It does not prescribe a retry, invent a status API, or promise that duplicates cannot occur.
