# Day 12 – Web Directory Scanning Investigation

## Scenario
Investigated a web server access log after an alert indicated possible directory scanning activity.

## Objective
- Identify suspicious web requests.
- Detect reconnaissance activity.
- Analyze HTTP status codes.
- Assess incident severity.
- Recommend the appropriate response.

## Tools Used
- cat
- grep
- wc

## Investigation Steps
1. Reviewed the web server access log.
2. Counted HTTP 404 responses.
3. Identified the source IP address.
4. Determined which resources were targeted.
5. Assessed whether the activity indicated reconnaissance.

## Findings
- Three requests returned HTTP 404.
- The requests targeted `/admin`, `/.git`, and `/backup.zip`.
- All suspicious requests originated from IP address `203.0.113.55`.
- The activity was consistent with directory scanning or reconnaissance.

## Conclusion
The investigation identified evidence of reconnaissance against the web server. Although no sensitive resources were successfully accessed, the repeated requests for common administrative and backup files warrant continued monitoring and further investigation if additional suspicious activity occurs.

## Lessons Learned
- Attackers often search for exposed files such as `.git` and `backup.zip`.
- HTTP 404 responses can still reveal attacker behavior.
- Reconnaissance is often the first stage of an attack.
- Decisions should always be based on the available evidence.
