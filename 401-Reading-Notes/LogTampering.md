## What is Log tampering?
Logs are designed to record nearly everything that occurs in a system, including hacking attempts, and can be the determining factor in catching hackers after their crime has been committed.

Ethical hackers need to understand how hackers tamper with logs, as it is a common practice with hackers.

### The process of covering your tracks
1. Disable auditing - This is the first step for hackers because if logging is turned off, there will be no trail of evidence. For windows systems, hackers can use the command line favorite, Auditpol
2. Clearing logs- clearlogs.exe, meterpreter
3. Modifying logs - a text editor may be needed to modify logs; regardless, it's as easy as modifying a Word file.
4. Erasing command history - the retained history of bash commands are found in the file ~/.bash_history
