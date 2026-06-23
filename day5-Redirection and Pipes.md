# Day 5 - Redirection and Pipes
## Commands Learned
- '>' (greater than sign)
- '>>' (double greater than sign)
- '|' (PIPE)
## What I Learned
### '>' (greater than sign)
#### Redirects output to a file and overwrites existing content
- Examples: cat security.log > report.txt
### '>>' (double greater than sign)
#### Appends output to a file without overwriting existing content
- Example: echo ''ERROR: Suspicious login attempt'' >> report.txt
### '|' (PIPE)
#### Sends the output of one command as input to another command
- Example: cat security.log | grep ERROR
## SOC Analyst Use Case
SOC analysts often use pipes and redirection to search large log files, filter events, and save investigation results
## Practice Commands
- cat security.log > report.txt
- echo ''ERROR: Suspicious login attempt'' >> report.txt
- cat security.log | grep ERROR
- cat security.log | grep ERROR > errors.txt
- cat security.log | grep ERROR | wc -l
## Key Takeaway
Redirection and pipes allow analysts to filter, save, and process log data efficiently
  
