## Statements
1. Count the number of processes of user `user` and print pairs `PID:command` for these processes.
2. Print `PID` of process which was launched last (with the last time of launch).
3. Write down to file `PID`s of processes which were launched by command which located at `/sbin/`.
4. For all processes count differences of resident and shared size of memory (in paged). Write down to file lines with format `PID:difference` sorted by decreasing of these differences.
5. For all registered processes print lines with format `ProcessID=PID : Parent_ProcessID=PPID : Average_Sleeping_Time=SleepAVG`. Sort this lines by parents' identifiers.
6. For each group print `Average_Sleeping_Children_of_ParentID=N is M`, where `N=PPID` and `M` is the average counted from `SleepAVG`.

## Some points of solutions
**ps**
- *-e, -A* - selects all processes.
- *-U userlist* - Select by real user ID (RUID) or name.  It selects the processes whose real user name or ID is in the userlist list.  The real user ID identifies the user who created the process.
- *-o format* - user-defined format.
