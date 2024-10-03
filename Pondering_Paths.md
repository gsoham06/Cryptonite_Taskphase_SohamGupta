Pondering Paths

1. The Root:
'/' is the root directory. The exact paths starting with root directory '/' are called 'absolute paths'.

2.Program and Absolute Paths:
'/' is also used as a directory separator. In this challenge we had to access a program stored in a directory which was stored in another directory. Used absolute path /challenge/run.

3. Position thyself:
cd command (change directory) is used to go to different directories. First ran /challenge/run and system showed that we need to be in  "/proc/67/fd" directory. So then cd to that directory and then ran absolute path /challenge/run.

4. Position Elsewhere:
Similarly used cd to change directory "/usr/share/zoneinfo/posix/Asia" and then used absolute path /challenge/run

5. Position Yet Elsewhere :
Again used cd to change directory to "/etc" and then used the absolute path /challenge/run.

6. Implicit Relative Paths:
Relative path does not start at root '/'. Path is relative to current working directory. Took a while to make sense of the hint. Changed directory to '/' first and used relative path challenge/run.

7. Explicit Relative Paths:
Tried /challenge/run but it is an absolute path which was not what the challenge required so had to cd to root directory '/' and then equivalent relative path ./challenge/run.

8. Implicit Relative Paths 2:
Linux has a safety measure. It does not search for programs in directory if we enter a naked path since we can accidentally run programs which share a common name with core system utilities. So after we change directory to /challenge, we use relative path ./run and not just run.

9. Home Sweet Home:
This one took me quite a bit of time and a lot of trial and error. Struggled with the argument part. In the end figured to use ~/r as argument.