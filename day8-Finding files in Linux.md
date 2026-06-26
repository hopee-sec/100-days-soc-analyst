# Day 8 - Finding Files in Linux
## Objectives
Learn how to search for files and locate commands in Linux using find, which and whereis
## Commands Practiced
### find
Used to search for files and directories
#### Examples:
- find . -type f - List all files in the currect directories
- find . -name '*.txt' - Searches for all .txt files
- find / -name hosts 2>/dev/null - Searches the entire system for files named hosts while hiding permission errors
### which
Shows the executable or alias that runs when you type a command
#### Example:
which grep
### whereis
Shows the location of a command and its manual page
#### Example: 
whereis grep
## Key Concepts Learned
- -name searches by filename
- -type f searches for regular files only
- * is a wildcard that matches any characters (e.g., *.txt finds all text files)
- 2>/dev/null hides permission error messages during searches
## SOC Relevance
These commands are useful for:
- Finding log files
- Locating configuration files
- Searching for suspicious files during security investigations
## What I Learned
Today i learned how to search for files efficiently using find, locate commands with which, and find executables and manual pages with whereis. I also learned how to suppress permission errors using 2>/dev/null, making system-wide searches cleaner and easier.
