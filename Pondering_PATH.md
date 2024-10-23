# Pondering PATH

**1. The PATH Variable**  
There is a special shell variable called `PATH` that stores directory paths. If you assign nothing to that variable, the shell cannot find programs. In this challenge, we had to blank out the `PATH` variable, export it, and then run the program.

**2. Setting PATH**  
To launch programs or scripts by just their name, we can set the `PATH` variable to their directory paths.

**3. Adding Commands**  
This challenge was a bit tricky. I could not figure out how to read or `cat` the flag. I kept making the mistake of changing the entire value of the `PATH` variable to the path of `win`. I just had to append the path of `win` to the `PATH` variable.

**4. Hijacking Commands**  
In this challenge, we had to trick the shell by creating our own `rm` command, which would `cat` the flag and then store its path inside the `PATH` variable.
