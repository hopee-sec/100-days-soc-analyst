# Day 7 - Process Management
## Commands Learned
### ps
Displays running processes
#### Example:
ps
### ps aux
Shows detailed information about all processes
#### Example:
ps aux
### top
Displays processes in real time and system usage
#### Example:
top
#### Useful keys:
- q = quit
- M = sort by memory
- P = sort by CPU
### kill
Terminates a process using its PID
#### Example: 
kill 3924
## Practice
### Created a process using:
sleep 300
### Found the process using:
ps aux | grep sleep
### Killed the process using:
kill PID
### verified that the process was terminated successfully
