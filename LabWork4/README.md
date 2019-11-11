## Statements
1. Create and run script (do not use if-else and other statement checking operators), which will try to create `test` directory in `home` directory. If directory creates successfully, script should write to file `~/report` message kind of `catalog test was created successfully` and creates in the directory file `Date_Time_of_Script_Launch`. Then in any case of last step script should try to `ping` to host [www.net_nikogo.ru](http://www.net_nikogo.ru/), and if host is unavailable, write to the end of `~/report` respective message.
2. Run previous script one more time after 2 minutes. Organize tracking to file `~/report` and print to console new lines at the moment they appear.
3. Run script from `1st` task every 5 minutes of every hour at the day of week, which you will be doing this task :).
4. Create 2 background processes, which will do the same infinite cycle (multiplication of 2 numbers, for example). After launch of processes virtual consoles should be available. Use command `top` to analyze percent of resources' using. First launched process should not use more than 20% of resources.
5. Process "Generator" sends information to process "Handler" through file. Process "Handler" should work with new lines this way: if line contains single "+" symbol, then process "Handler" should switch to "add" mode and wait integer numbers from input. If line contains single "*", process "Handler" should switch to "multiplication" mode and wait integer numbers. If line contains integer, then handler should calculate current active operation (chosen mode) on current value of calculating variable. At the launch of script mode is "add", and calculating variable's value is 1. If given line equals to "QUIT", script should print respective message and finish his work. In any other case, process should print an error message.
6. Process "Generator" reads data from console while read value is not equal to "TERM". In this case it should send system signal `SIGTERM` to process "Handler". Process "Handler" should intercept signal `SIGTERM` and finish end process by printing respective message.
7. Process "Generator" reads data from console in infinite cycle. If given line contains single "+" symbol, it sends user signal `USR1`. If line contains single "*" symbol, generator sends to handler signal `USR2`. If line contains word `TERM`, generator sends to handler `SIGTERM` signal. Other lines should be ignored. Initial value of calculating variable is 1. Handler adds or multiplies calculating variable's value to 2 and prints its value. Calculations should be done once per second. If handler receives `SIGTERM` signal, it ends process.

## Some points of solutions
**mkdir**
- creates directory

**touch**
- creates file

**ping** -c --count
- Stop  after  sending  --count  ECHO_REQUEST packets. With deadline option, ping waits for --count ECHO_REPLY packets, until the time‐out expires.
at - command schedules a command to be run once at a particular time that you normally have permission to run.
at -f - schedules a file to be run.

**crontab**
- schedules a command to be run periodically.

**nice** -n N
- add integer N to the niceness (default 10)

**command&**
- run at background mode
**tail** -n 0
- prevents reading from a file until its contents are updated after running the `tail` command