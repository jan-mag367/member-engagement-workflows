# Workflow: Member feedback

## Goal
Collect feedback efficiently and route it to the right people with a clear audit trail.

## Inputs (Form)
- Category (dropdown): workplace issue / comms / training / support / other
- Message (long text)
- Optional: preferred contact method (email/phone) (only if needed)

## Storage (SharePoint List)
List name: FeedbackLog
Fields:
- DateSubmitted
- Category
- Summary
- Status (New / In Review / Closed)
- Owner (person)
- Notes (internal)

## Automation (Power Automate)
1. Trigger: When a new Forms response is submitted
2. Action: Create item in SharePoint list (FeedbackLog)
3. Action: Notify mailbox/Team channel (based on Category)
4. Action: Optional acknowledgement message (no sensitive details)

## Permissions
- Only officers/admins can see the full list
- If collecting contact info, restrict access further
