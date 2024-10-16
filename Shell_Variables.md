Shell Variables:

1. Printing Variables:
echo command is used to print things. Just using echo FLAG the echo command takes FLAG as a string argument. To print FLAG variable we add a $ before the var name. echo $FLAG gives the flag for the challenge.

2. Setting Variables
We can also assign values to variables like we do in any programming language. We should just make sure there is no space around the '='.

3. Multi-word Variables
We can't use space around '=' so we cannot assign multiple words to Variable by itself. We need to enclose it in "".

4.Exporting Variables
Variables are local to a shell process. To access them in another shell session, we need to export them using keyword 'export'.

5. Printing Exported Variables
The env command prints out every exported variable in my shell.

6. Storing command output
We can store the out of a program or command with $(). In this challenge we had to store output of /challenge/run to PWN using PWN=$(/challenge/run)
and then echo PWN to get the flag.

7. Reading Input
read lets the user input through standard input. We use -p to to separate a prompt and input.

8. Reading Files
We use the concept of redirecting standard input in this challenge to read a content of a file into a varibale PWN.