# Pondering Paths

1. **The Root**:  
   `'/'` is the root directory. Exact paths starting with the root directory `'/'` are called **absolute paths**.

2. **Program and Absolute Paths**:  
   `'/'` is also used as a directory separator. In this challenge, we had to access a program stored in a directory within another directory. Used the absolute path `/challenge/run`.

3. **Position Thyself**:  
   The `cd` command (change directory) is used to navigate between directories. First, ran `/challenge/run` and the system indicated that we needed to be in the `"/proc/67/fd"` directory. So, I used `cd` to change to that directory and then ran the absolute path `/challenge/run`.

4. **Position Elsewhere**:  
   Similarly, I used `cd` to change to the directory `"/usr/share/zoneinfo/posix/Asia"` and then used the absolute path `/challenge/run`.

5. **Position Yet Elsewhere**:  
   Once again, used `cd` to navigate to the directory `"/etc"` and then ran the absolute path `/challenge/run`.

6. **Implicit Relative Paths**:  
   A relative path does not start from the root `/`. The path is relative to the current working directory. After some time, I understood the hint. Changed directory to `'/'` first and used the relative path `challenge/run`.

7. **Explicit Relative Paths**:  
   Initially tried `/challenge/run`, but that is an absolute path, which wasn't required for the challenge. So, I `cd` to the root directory `'/'` and used the equivalent relative path `./challenge/run`.

8. **Implicit Relative Paths 2**:  
   Linux has a safety measure where it does not search for programs in directories if we enter a naked path. This prevents accidentally running programs that share names with core system utilities. After changing to the `/challenge` directory, I used the relative path `./run`, not just `run`.

9. **Home Sweet Home**:  
   This one took considerable trial and error. I struggled with the argument part but eventually figured out to use `~/r` as the argument.
