## Statements
1. Create file `errors.log`. Write down to it all lines from accessible for reading files of `/var/log/` directory, which starts with `ACPI` without names of files. Print those lines which contain full names of files.
2. Create file `full.log` and write down to it all lines from `/var/log/Xorg.0.log` which contain warnings and informational messages by replacing their marks to `Warning:` and `Information:` respectively. Print errors first, then warnings. Print the content of this file to console.
3. Create file `emails.lst` and write down to it all the emails from all of the files of `/etc` directory.
4. Find all scenario files from `/bin` and print the interpreter which occurs the most.
5. Print the list of users with their `UID` sorting by `UID`. You can find information about users at `/etc/passwd`.
6. Count the total number of words on files of `/var/log` directory which has `.log` format.
7. Print three most frequent words from the result of `man bash`.

## Some points of solutions
**grep**
- *-h* - Suppress  the  prefixing  of  file names on output.  This is the default when there is only one file (or only standard input)  to search.
- *-r* - Read all files  under  each  directory,  recursively,  following symbolic  links only if they are on the command line.  Note that if  no  file  operand  is  given,  grep  searches  the   working directory.  This is equivalent to the -d recurse option.
- *-E* - Interpret PATTERN as an extended regular  expression.
- *-o* - Print  only  the  matched  (non-empty) parts of a matching line, with each such part on a separate output line.

**cut**
- *-d, --delimiter=DELIM* - use DELIM instead of TAB for field delimiter.
- *-f, --fields=LIST* - select only these fields;  also print any line that contains no delimiter character, unless the -s option is specified.

**xargs**
- *-n* - Use  at  most  max-args  arguments per command line.  Fewer than max-args arguments will be used if the size (see the -s  option) is  exceeded, unless the -x option is given, in which case xargs will exit.

**uniq**
- *-c* - prefix lines by the number of occurrences.

**sort**
- *-r* - reverses the result.
- *-n* - compares numerical values.
