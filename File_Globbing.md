File Globbing

1. Matching with * :
When we use * with any file name as argument, the shell tries to replace the * with possible files that match the pattern. In this challenge we had to cd to /challenge but using /ch* as an argument and then run /challenge/run. The shell can replace * with a string.

2. Matching with ? :
Works very similarly to * but unlike *, the shell only tries to find replacements of ? with a character.

3. Matching with [] :
It works like ? but it limits the matching set. The shell only matches with the characters specified inside the square brackets []. Pass file_[bash] as argument to /challenge/run.

4.Matching paths with []:
We can glob with absolute paths as well. In this challenge we gave /challenge/files/file_[bash] as absolute path argument to /challenge/run.

5. Mixing globs:
We can use different types of globbing together. In this challenge after cding to /challenge/files, I first used echo Look: * (same as ls I now realise) to see the names of all the files available. Took me a while but observed that only challenge educational and pwning started with either c e or p. So gave [cep]* as argument to challenge/run.

6. Exclusionary globbing:
Using ! or ^ with [] we can match with all the files not containing the character in []. In this challenge we use [!pwn]* as an argument to /challenge/run.