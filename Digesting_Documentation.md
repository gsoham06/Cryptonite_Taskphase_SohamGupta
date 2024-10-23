# Digesting Documentation

1. **Learning from Documentation**  
   Proper specification of arguments to commands and programs is crucial to ensure correct execution. I passed `--giveflag` as an argument to the program `/challenge/challenge`.

2. **Learning Complex Usage**  
   Sometimes, we may need to pass arguments to other arguments. In this challenge, I had to pass the location of the flag as an argument to `--printfile`. First, I used `find "flag"` to locate the flag.

3. **Reading Manuals**  
   Using `man` with any command gives us the manual for that command. This is a very helpful tool since using commands can sometimes get complicated and difficult to remember.

4. **Searching for Manuals**  
   Running `man man` provides the manual for the `man` command itself, which shows all its advanced uses. I used the `--regex` argument with "challenge" to find the flag.

5. **Helpful Programs**  
   Not all programs have a manual. However, if we use `-h` or `--help` as an argument with those programs, they often provide usage instructions. In this case, the program was `/challenge/challenge`, and the argument was `-h`. It informed me to pass `-p` as an argument first to get the secret key, and then `-g` with the key to retrieve the flag.

6. **Help for Builtins**  
   Some commands are built into the shell and are handled internally. We don't use `man` or `-h` with builtins; instead, we use `help`. Running `help` by itself gives a list of built-in commands, and using `help` followed by a specific command provides details for that command only.
