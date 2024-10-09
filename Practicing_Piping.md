Practicing Piping

1. Redirecting output:
Linux uses 3 channels for communication. The command echo gives output in output channel but we can redirect to a file using >.

2. Redirecting more output :
> can be used with any command to redirect output channel. In this challenge we had to redirect output of /challenge/run to myflag and then cat myflag.

3. Appending output:
> overwrites the current content in the file. It will create a new output file every time and delete old contents. To append new content to the old one, we need to use >>.

4. Redirecting errors:
File descriptor is a number which specifies which channel. 2> specifies that the channel being redirected is error channel. We can redirect multiple channels/file descriptors at the same time. In this challenge we had to redirect standard output to myflag using > or 1> and standard error to instructions using 2>.

5. Redirecting input:
Just like we redirect output, we can redirect input from a file into a program using <. In this challenge we had to redirect output COLLEGE into PWN first and then redirect PWN into /challenge/run.

6. Grepping stored results:
Had to use 2 different concepts for this challenge. First we had to redirect the output of /challenge/run to file and then grep for flag with pattern pwn.college in that file.

7. Grepping live output:
It is not necessary to redirect output to a file and then grep in that file. We can use a pipe operator | to connect standard output from the left side to standard input on the right side.

8. Grepping errors:
We can redirect from 1 file descriptor to another like 2>&1 which redirects standard error to output. In this challenge we needed to pipe output and grep for pwn college but /challenge/run gave output on standard error. So we needed to redirect is to standard output using 2>&1 and then pipe into grep.

9. Duplicating piped data with tee:
When we pipe data, it is not visible. We can use tee to "intercept" the data and sends it to any file we specify. We can then cat the file to see the data. In this challenge we had to intercept the output of /challenge/pwn and save it in a temp file and then use the secret hint in the output to get flag.

10. Writing to multiple programs
Linux and the shell allows you to use any command/utility that takes file arguments and hook it up to the input or output side of a program. >() creates a temporary file which is hooked to input of the command. In this challenge we had to pip /challenge/hack into the commands /challenge/the and /challenge/planet which I did using | tee >(/challenge/the) >(/challenge/planet).

11. Split - piping stderr and stdout
This last challenge was tricky. Took me a while and the hint int he description "deep knowledge of |" threw me off. For this challenge I used /challenge/hack 2> >(/challenge/the) > >(/challenge/planet).
