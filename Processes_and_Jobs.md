# Processes and Jobs

1. **Listing Processes:**  
   The `ps` command lists processes. On its own, it's not very informative, but we can make it more useful by adding arguments. For example, `-ef` shows parent process IDs, and `aux` gives CPU and memory usage percentages for each process.

2. **Killing Processes:**  
   Just like in a task manager, we can terminate or kill a process using the `kill` command in Linux. We need to pass the process ID (PID) as an argument to kill the specific process.

3. **Interrupting Processes:**  
   If a process is clogging or slowing down the terminal, we can interrupt it using `Ctrl + C`, which stops the process immediately.

4. **Suspending Processes:**  
   If we don’t want to stop a process entirely, we can suspend it and send it to the background by pressing `Ctrl + Z`.

5. **Resuming Processes:**  
   To bring a suspended process back to the foreground, we can use the `fg` command.

6. **Backgrounding Processes:**  
   To resume a suspended process but keep it running in the background, we can use the `bg` command.

7. **Foregrounding Processes:**  
   A background process can be brought directly to the foreground by using the `fg` command.

8. **Starting a Backgrounded Process:**  
   We can directly start a process in the background by appending `&` at the end of the command, instead of suspending and backgrounding it manually.

9. **Process Exit Codes:**  
   Every shell command exits with an exit code. A successful command typically returns 0, while a failure returns a non-zero value. To access the exit code of the most recently terminated command, we use the special `$?` variable to check its value.
