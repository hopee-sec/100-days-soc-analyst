# Day 9 - SOC Investigation: SSH Authentication Logs

## Scenario
Investigated suspicious SSH login activity on a Linux server.

## Objective
Determine whether the login attempts were suspicious and identify successful logins.

## Tools Used
- grep
- cat
- wc

## Findings
- Total failed login attempts:
- Total successful logins:
- User accounts affected:
- Suspicious IP addresses:
- Severity:

## Conclusion
The investigation identified multiple failed SSH login attempts targeting several user accounts, followed by successful logins for the admin and john accounts. The pattern is consistent with a possible brute-force attack, particularly because successful authentication occurred after repeated failures. Due to the potential compromise of privileged accounts, this incident should be escalated for further investigation, including verification of user activity and the source IP addresses.

## Lessons Learned
- Failed logins don't always mean an attack succeeded.
- A successful login after several failed attempts deserves further investigation.
- Evidence should be collected before escalating an incident.
