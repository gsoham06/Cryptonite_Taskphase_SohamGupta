# Comprehending Commands

1. **cat: Not the Pet, but the Command**  
   `cat` is used to read out files. It can also concatenate multiple files if specified.

2. **Catting Absolute Paths**  
   We can use absolute paths as `cat` arguments as well.

3. **More Catting Practice**  
   Provided a specified absolute path as an argument to `cat`.

4. **Grepping for a Needle in the Haystack**  
   The `grep` command is used to find lines containing a specific string in a file.

5. **Listing Files**  
   The `ls` command lists all files in directories provided as arguments.

6. **Touching Files**  
   `touch` is used to create a blank file, with the name given as an argument. First, navigate to the desired directory using `cd`, then use `touch` to create the file.

7. **Removing Files**  
   The `rm` command deletes a file. The file name to remove is provided as an argument.

8. **Hidden Files**  
   By default, `ls` does not list all files. Files that start with `.` are hidden. Use `ls -a` to view them. In this challenge, I used `ls / -a` to locate the flag file and then used `cat` to read the flag file.

9. **An Epic Filesystem Quest**  
   This was a lengthy procedure. I had to use `ls`, `cd`, and `cat` multiple times, navigating through several directories and reading files to eventually find the flag.

10. **Making Directories**  
    The `mkdir` command is used to create a directory, followed by the desired directory name.

11. **Finding Files**  
    Use the `find` command to search for files. I searched for all locations where the file "flag" was stored and used `cat` on each path one by one until the flag was found.

12. **Linking Files**  
    We can link one file to another using `ln`. `ln` creates hard links, while `ln -s` creates soft links or symbolic links. In this challenge, I linked `/home/hacker/not-the-flag` to `/flag` and then ran `/challenge/catflag`.
