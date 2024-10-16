Processes and Jobs

1. Listing Processes:
The ps command lists processes. Pretty pointless on its own so to make it useful we pass with arguments. Argument -ef gives parent process id and aux gives percentage of total cpu and memory a process is using.

2. Killing Processes:
Like we end tasks in task manager, we can kill/terminate process using command kill in Linux. We need to pass the PID of the process we want to kill as an argument to the command.

3. Interrupting Processes
To get rid of a process which is clogging or slowing up our terminal, we can use ctrl c and it will get rid of your process.

4. Suspending Processes
If we don't want to take such drastic measures like interrupting a process then we can suspend a process to the background with Ctrl z.

5. Resuming Processes
To resume a suspended process in the foreground we use the command fg.

6. Backgrounding Processes
To resume a suspended process in the background we can use a bg.

7. Foregrounding Processes
We can bring a process from a background to foreground directly by just using fg command

8. Starting Backgrounded Process
We don't need to suspend and then background a process for it to run in the background. We can directly start it in the background by adding '&' at the end of command.

9. Process Exit Codes
Every shell commands exits with an exit code. If the command/process was successful then its typically returns 0 and commands that fail return a non zero value. To access this exit code of the most recently terminated command we use the special '?' variable prepended by $ to read its value. 