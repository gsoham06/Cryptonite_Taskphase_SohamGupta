# Practicing Piping

1. **Redirecting Output:**  
   Linux uses three channels for communication. The `echo` command outputs to the output channel, but we can redirect this output to a file using `>`.

2. **Redirecting More Output:**  
   `>` can be used with any command to redirect the output channel. In this challenge, I redirected the output of `/challenge/run` to `myflag` and then used `cat myflag` to read it.

3. **Appending Output:**  
   `>` overwrites the content of the file. To append new content to an existing file without overwriting it, we use `>>`.

4. **Redirecting Errors:**  
   A file descriptor is a number that specifies which channel to redirect. `2>` indicates that we're redirecting the error channel. In this challenge, I redirected standard output to `myflag` using `>` or `1>`, and standard error to `instructions` using `2>`.

5. **Redirecting Input:**  
   Just like we redirect output, we can redirect input from a file into a program using `<`. In this challenge, I redirected the output `COLLEGE` into `PWN` first and then redirected `PWN` into `/challenge/run`.

6. **Grepping Stored Results:**  
   This challenge required two steps. First, I redirected the output of `/challenge/run` to a file, then used `grep` to search for the pattern `pwn.college` in that file.

7. **Grepping Live Output:**  
   It’s not necessary to redirect output to a file before using `grep`. We can use the pipe operator `|` to connect the standard output from one command directly into the input of another command.

8. **Grepping Errors:**  
   We can redirect one file descriptor to another, like `2>&1`, which redirects standard error to standard output. In this challenge, I piped the output of `/challenge/run` into `grep`, but since the output was on standard error, I first redirected it to standard output using `2>&1` and then piped it into `grep`.

9. **Duplicating Piped Data with tee:**  
   When piping data, it’s not directly visible. We can use `tee` to "intercept" the data and send it to a file while still piping it forward. In this challenge, I intercepted the output of `/challenge/pwn`, saved it in a temp file, and used the secret hint in the output to get the flag.

10. **Writing to Multiple Programs:**  
   Linux allows you to hook up the output of a program to multiple commands. `>()` creates a temporary file that connects to the input of a command. In this challenge, I piped `/challenge/hack` into `/challenge/the` and `/challenge/planet` using `| tee >(/challenge/the) >(/challenge/planet)`.

11. **Split - Piping stderr and stdout:**  
   This last challenge was tricky. It required deep knowledge of pipes. I used `/challenge/hack 2> >(/challenge/the) > >(/challenge/planet)` to handle both standard error and standard output and redirect them to different programs.
