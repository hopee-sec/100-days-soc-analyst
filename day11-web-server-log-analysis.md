# Day 11 – Web Server Access Log Analysis

## Scenario
Investigated web server access logs after alerts reported unusual web activity. The objective was to distinguish normal user behavior from suspicious authentication attempts and reconnaissance activity.

## Objective
- Analyze HTTP status codes.
- Identify suspicious IP addresses.
- Detect possible password guessing.
- Detect reconnaissance attempts.
- Assess incident severity.
- Recommend an appropriate response.

## Tools Used
- cat
- grep
- wc

## Investigation Steps
1. Created and reviewed the web server access logs.
2. Counted HTTP response codes (200, 401, 403, and 404).
3. Identified IP addresses associated with suspicious requests.
4. Analyzed authentication attempts and access to restricted resources.
5. Distinguished legitimate web traffic from suspicious activity.
6. Determined the severity of the incident based on the available evidence.

## Findings
### Investigation 1
- 3 requests returned HTTP 401.
- 2 requests returned HTTP 403.
- 4 requests returned HTTP 200.
- IP address **203.0.113.50** generated repeated unauthorized login attempts before a successful login.
- IP address **198.51.100.20** attempted to access the restricted `/admin` page.

### Investigation 2
- 6 requests returned HTTP 200.
- 2 requests returned HTTP 401.
- 1 request returned HTTP 403.
- 2 requests returned HTTP 404.
- IP address **198.51.100.45** attempted to access the `/admin` page and later authenticated successfully after failed login attempts.
- IP address **203.0.113.80** attempted to access sensitive files such as `.env` and `config.php`, indicating possible reconnaissance activity.

## Conclusion
The investigations identified multiple suspicious web activities, including repeated failed authentication attempts, access to restricted resources, and requests for sensitive configuration files. Although these activities indicate possible password guessing and reconnaissance, additional evidence such as authentication logs, application logs, and firewall logs would be required before confirming a compromise and escalating the incident.

## Lessons Learned
- HTTP status codes provide valuable information during web server investigations.
- A successful login is not automatically malicious; surrounding events must be considered.
- Requests for sensitive files like `.env` and `config.php` may indicate reconnaissance.
- Incident severity should be determined using evidence, not assumptions.
- Different log types require different investigation techniques and careful interpretation.
