# Untangling Users

**1. Becoming root with su**  
The switch user command `su` starts a root shell, but before starting the root shell, it will ask for the root password. In this challenge, we had to start a root shell using `su` and then `cat` the flag.

**2. Other users with su**  
With no arguments, `su` will start a root shell, but we can also specify if we want to switch to another user by passing the username as an argument.

**3. Cracking Passwords**  
Passwords are stored in `/etc/shadow` in Linux. There are sometimes leaks in passwords. With the acquired hash value of the password, we can use something called a John The Ripper tool, which is an open-source password recovery tool available for multiple operating systems. We use the command `john` to use the tool.

**4. Using sudo**  
`su` is a thing of the past now; root passwords often leak and are hard to maintain. So to run a program as admin, `sudo` is used. `sudo` does not require a password to authenticate, and it does not change the user.
