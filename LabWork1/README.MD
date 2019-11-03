## Statements
1. Given two strings as parameters. Print a message on their equality.
2. Given three integers as parameters. Print the biggest one.
3. Read strings till string `"q"`, then print all read strings concatenated.
4. Read integers till the first even number, then print the number of read numbers.
5. Create a text menu with four points. For chosen point run `nano`, `vi` editor, `links` browser or exit menu respectively.
6. If the script is ran from home directory print path to home directory and exit with code `0`, else print error message and exit with code `1`.

## Some points of solutions
1. We can just use `==` operation to check strings' equality.
2. I decided to find the biggest number not only if there are three parameters, that's why I use `for parameter in "$@"` instuction to iterate over all given parameters. I used standard `if` instruction to change answer and `-lt` to compare numbers. 
3. In third task I just used `while` instruction to iterate till string `q` and just contatenated every given string to variable `answer` by using operation `+=`.
4. We must use `-eq` to compare numbers!
6. Our task is just compare two following strings with `==`:
- `$PWD` gives current working directory.
- `$HOME` gives home directory.