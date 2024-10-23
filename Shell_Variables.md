# Shell Variables

1. **Printing Variables:**  
   The `echo` command is used to print things. If we use `echo FLAG`, it takes "FLAG" as a string argument. To print the value of a variable, we add a `$` before the variable name. For example, `echo $FLAG` prints the value of the `FLAG` variable.

2. **Setting Variables:**  
   We can assign values to variables, similar to other programming languages. Just ensure there's no space around the `=` sign when setting a variable.

3. **Multi-word Variables:**  
   Since we can't have spaces around `=`, we need to enclose multiple-word values in quotes when assigning them to variables, like `VAR="multiple words"`.

4. **Exporting Variables:**  
   By default, variables are local to the shell process. To make them available in another shell session or subprocess, we use the `export` command.

5. **Printing Exported Variables:**  
   The `env` command prints all the exported variables in the current shell.

6. **Storing Command Output:**  
   We can store the output of a command in a variable using `$()`. For example, `PWN=$(/challenge/run)` stores the output of `/challenge/run` in the `PWN` variable, and then we can use `echo $PWN` to print the stored output.

7. **Reading Input:**  
   The `read` command allows user input via standard input. We can use the `-p` flag to display a prompt before reading the input.

8. **Reading Files:**  
   In this challenge, we used input redirection to read the contents of a file into a variable, for example, reading into `PWN` using `PWN=$(<file)`.

