# Day 13 – Log Correlation: Web & Authentication Logs

## Scenario
Investigated a security alert involving repeated failed web login attempts followed by a successful authentication. The objective was to correlate data from multiple log sources to determine whether the activity was suspicious.

## Objective
- Correlate web server and authentication logs.
- Identify repeated failed login attempts.
- Match source IP addresses across different logs.
- Assess the severity of the incident.
- Recommend appropriate response actions.

## Tools Used
- cat
- grep
- wc

## Investigation Steps
1. Reviewed the web server access log.
2. Counted HTTP 401 responses.
3. Identified the IP address responsible for the failed login attempts.
4. Correlated the IP address with the authentication log.
5. Identified the account that successfully authenticated.
6. Assessed the incident and determined the appropriate response.

## Findings
- Two HTTP 401 responses were recorded.
- IP address **203.0.113.55** generated the failed login attempts.
- The same IP address successfully authenticated to the **admin** account.
- Other successful logins for **alice** and **backup** appeared to be normal.
- The activity required further investigation before confirming a compromise.

## Conclusion
The investigation revealed repeated failed web login attempts followed by a successful authentication from the same IP address. While this pattern may indicate password guessing, additional evidence such as authentication history and post-login activity is required before confirming malicious activity. The incident should remain under investigation and be escalated if further suspicious behavior is identified.

## Lessons Learned
- Correlating multiple log sources provides better context than analyzing a single log.
- A successful login after failed attempts is suspicious but does not automatically confirm a compromise.
- Administrator accounts require extra attention because they have elevated privileges.
- Incident decisions should always be based on evidence rather than assumptions.
