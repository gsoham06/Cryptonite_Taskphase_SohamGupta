Perceiving Permissions

1. Changing File Ownership
Every file in Linux is owned by a user. The root user is at the top/admin. It has access to all files. To change ownership of a file we use chown command which can only be used by root user.

2. Groups and Files
Files have an owning user and group. A group can have multiple users in it. This exists for easier sharing. For this challenge we had to use chgrp to change group ownership to hacker group (the group in which the hacker user is in) and then cat /flag.

3. Fun with Groups Names
Every user has their own group by convention but that does not always have to be the case. In this challenge we had to use the command id to find which group we are in, the change group ownership of flag to that group and then cat flag.

4. Changing Permissions
File permissions can also be changed like ownership with chmod command. Usually user needs to have write access to file to change its permissions. I kept using chmod u+r in this challenge which was wrong since hacker did not have ownership, took me a while to figure that the solution was chmod +r.

5. Executable Files
Used chmod +x to give executing permission.

6. Permission Tweaking Practice
8 rounds of racking my brain changing permission of /challenge/pwn.

7. Permission Setting Practice
8 more rounds of labour work which took me longer than it should have because of small errors. We do not individually need to remove and add permission use +/-, we can set it entirely at once using =.

8. The SUID Bit
Setting a file's SUID bit using chmod lets  a user to run that program as as the owner of that program file.
In this challenge we had to set SUID by chmod u+s.
