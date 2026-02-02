# Workflow: Volunteer sign-up and routing

## Goal
Capture volunteer interest and route tasks to organisers with tracking.

## Inputs (Form)
- Area of interest (checkboxes): comms / outreach / events / research / admin
- Availability (short text)
- Skills (optional)
- Contact email (required)

## Storage (SharePoint List)
List name: VolunteerRegister
Fields:
- Name (optional)
- Email
- Interests
- Availability
- Status (New / Contacted / Active / Paused)
- AssignedTo (person)
- Notes

## Automation (Power Automate)
1. Trigger: New form response
2. Create/Update: SharePoint list item
3. Route:
   - If “events” → notify Events lead
   - If “comms” → notify Comms lead
4. Optional: Send confirmation email to volunteer
