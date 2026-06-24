# Day 6 - Text Processing and Log Analysis
## Objectives
Learn how to search, filter, count, and sort text data in Linux
## Commands Practiced
### grep
Searches for specific text patterns in a file
#### Examples:
- grep ''ERROR'' sample.txt
- grep -n ''SSH'' sample.txt
- grep -v ''INFO'' sample.txt
### wc
Counts lines, words, and characters
#### Examples: 
- wc sample.txt
- wc -l sample.txt
### sort
Sorts text alphabetically
#### Example: 
sort sample.txt
## Key Takeaway
- grep is useful for finding specific log entries
- grep -n displays line numbers
- grep -v excludes matching lines
- wc -l counts the number of lines in a file
- sort organizes text alphabetically
## Practical Exercise
Analysed a sample log file and identified error entries, suspicious activities and failed login attempts using grep and wc 
