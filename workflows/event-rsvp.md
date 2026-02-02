# Workflow: Event RSVP and reminders

## Goal
Track attendance and send reminders without manual chasing.

## Inputs (Form)
- Name
- Email
- Attendance: Yes / No / Maybe
- Accessibility needs (optional)

## Storage (SharePoint List)
List name: EventRSVP
Fields:
- EventName
- Name
- Email
- Attendance
- Notes

## Automation (Power Automate)
1. Trigger: New RSVP
2. Save to SharePoint list
3. Reminder:
   - Scheduled flow 24h before event
   - Email only to "Yes" and "Maybe"
4. Post-event:
   - Optional follow-up feedback form link
