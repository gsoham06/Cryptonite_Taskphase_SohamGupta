Comprehending Commands

1. cat : not the pet, but the command
cat is used to read out files. It can also concatenate multiple files if specified.

2. catting absolute paths
We can use absolute paths as cat arguments as well

3. more catting practice
Gave specified absolute path as argument to cat

4. grepping for a needle in the haystack
grep command is what we need to use when we need to find lines containing a specific string in a file.

5. listing files
ls command lists all files in directories we provide as argument

6. touching files
touch is used to create a blank file and we give name as argument. We cd to the directory we want to create the file in and then use touch.

7. removing files
rm is command we use to remove/delete a file. The file name we want to remove is put as an argument.

8. hidden files
ls does not list all files by default. Files starting with '.' are not visible with ls. We must use ls -a to view the files. Used ls / -a in this challenge to see the flag file and used cat with the flag file.

9. An Epic Filesystem Quest
Was a very long procedure. Had to play around with ls and cd and cat multiple times and after going to multiple directories and reading multiple files, finally got the  flag.

10. making directories
We can make directories using command mkdir followed by directory name we want to give.

11. finding files
Use find command to search for files, We first search for all location where file flag is stored and then we cat to each path one by one and see if it gives us flag.

12. linking files
We can link one file to another using ln. ln makes hard links which ln -s makes soft links or symbolic links. In this challenge we had to link /home/hacker/not-the-flag to /flag and then run /challenge/catflag.