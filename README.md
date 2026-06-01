1. Daily Task Submission and Row-Reset Automation
Trigger: Clicking the "Submit Task" macro button on the Daily Work Log sheet.

Mechanism: The script intercepts data entered exclusively in Row 2 (Task Details, Start/End Dates, Status, Comments).

Action: It instantly transfers this data payload into a hidden historical ledger or master database running in the background. Once the transfer completes safely, the script executes a clear command to completely reset Row 2, leaving it blank and ready for the next entry.

2. Dashboard Master Submission and Final Data Lock
Trigger: Clicking the master "Submit" button located on the primary Dashboard.

Mechanism: A centralized compilation routine gathers all operations logged throughout that calendar date.

Action: It packages the aggregated logs and commits them securely to the organization's overarching central server/database, creating an immutable, non-editable record of the employee's output for that day.

3. Chronological Parsing & Automatic Time Categorization
Trigger: Entering a specific calendar date in either the Monthly or Daily log sheets.

Mechanism: Background calculation engines and array formulas instantly evaluate the day, month, and year values.

Action: Without requiring manual sorting by the employee, the sheet automatically parses the timestamp and auto-fills metadata such as the exact Month and designated fiscal/calendar Week (e.g., Week 1, Week 4, Week 5) for clean data organization.

4. The 11:31 PM Automated Compliance Check (Time-Driven Trigger)
Trigger: A server-side Time-Driven Cron Trigger set to execute automatically every single night at exactly 11:31 PM. This runs independently on Google Cloud servers, meaning it triggers even if the employee's computer is entirely powered down.

Mechanism: The script scans the sheet arrays to evaluate if the employee has successfully pushed updates or clicked the Master "Submit" button before the organizational curfew.

5. Automated Attendance Penalty and Email Escalation System
Trigger: A failed validation flag caught during the 11:31 PM Time-Driven compliance check (i.e., an unmarked task status or an unsubmitted sheet).

Mechanism: This utilizes administrative permission integrations to communicate cross-platform.

Action: * Email Dispatched: The system automatically drafts and fires an immediate alert using the employee's email credentials to both Human Resources (HR) and the Head of Department (HOD) notifying them of non-compliance.

Status Override: Simultaneously, the script communicates via API with the company’s internal database to instantly mark the employee’s status as "Absent" for that shift.

6. Background Script Impersonation & OAuth Execution
Trigger: One-time global security authorization completed via the Google Workspace sign-in screen using the corporate email extension (@space-india.com).

Mechanism: Integrates advanced Workspace API permissions (Sheets API, Gmail API, and script execution hooks).

Action: This automation establishes administrative impersonation scopes. It explicitly permits the code backend to automatically:

Read, modify, compose, and send email records on behalf of the user.

Run silently in the background when the user is completely offline or not present on the document, ensuring deadlines and reporting steps are executed seamlessly without requiring manual daily authorization prompts.
