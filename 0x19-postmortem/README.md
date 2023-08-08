# Postmortem

## Issue Summary
Between 11:50 and 12:20 on July 27, 2023, 30 customers experienced SQL Server problems. The event was triggered by a new deployment. This event was detected using the monitoring tool. 420 queries were incorrectly sent to the server, 12% of the queries over the course of 30 minutes.

## Issue Timeline
- Detected between 11:50 and 12:20, July 27, 2023 when the SQL Server alert was triggered and DBA Team were paged.
- The event was mitigated by fixing the invalid parameters of SQL queries. This P2 incident affected 5% of customers 
- SQL parameters in the code are fixed and deployed
- SQL Scripts should always be re-checked in the test environment when code is merged before deployment.

