# Day 10 – SOC Investigation: Authentication Log Analysis & Incident Prioritization

## Scenario
Investigated multiple SSH authentication alerts to determine whether the activities were legitimate or indicative of a security incident.

## Objective
- Analyze authentication logs.
- Identify failed and successful login attempts.
- Detect suspicious IP addresses and targeted accounts.
- Assess the severity of the incident.
- Recommend the appropriate response.

## Tools Used
- cat
- grep
- wc

## Investigation Steps
1. Reviewed authentication logs.
2. Counted failed and successful login attempts.
3. Identified usernames and source IP addresses.
4. Determined which IP generated the most failed logins.
5. Distinguished between normal and suspicious authentication activity.
6. Assessed the severity of the incident.
7. Recommended the appropriate response based on the evidence collected.

## Findings
- 8 failed login attempts.
- 4 successful login attempts.
- Multiple user accounts appeared in the logs.
- IP address **203.0.113.88** generated the highest number of failed login attempts against multiple accounts.
- Normal authentication activity was observed for **alice** and **backup**.
- A successful login for **david** required verification to determine whether it was legitimate.

## Conclusion
The investigation identified suspicious authentication attempts from a single IP address targeting multiple user accounts. Although no unauthorized successful login was confirmed, the repeated failed attempts required further investigation. Based on the available evidence, the incident should remain under investigation until additional context confirms whether the activity is malicious or legitimate.

## Lessons Learned
- Security incidents should be assessed using evidence rather than assumptions.
- Multiple failed login attempts do not always indicate a successful compromise.
- A single suspicious IP targeting multiple accounts deserves higher priority.
- Legitimate users may occasionally fail to log in due to mistyped passwords.
- Incident severity should be adjusted as new evidence becomes available.
