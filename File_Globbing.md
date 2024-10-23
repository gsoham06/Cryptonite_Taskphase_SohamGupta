# File Globbing

1. **Matching with \***  
   When we use `*` with any file name as an argument, the shell tries to replace `*` with possible files that match the pattern. In this challenge, I navigated to `/challenge` using `/ch*` as an argument and then ran `/challenge/run`. The shell can replace `*` with a string.

2. **Matching with ?**  
   `?` works similarly to `*`, but unlike `*`, the shell only replaces `?` with a single character.

3. **Matching with []**  
   This works like `?`, but it limits the matching set. The shell only matches characters specified inside square brackets `[]`. I passed `file_[bash]` as an argument to `/challenge/run`.

4. **Matching Paths with []**  
   We can glob with absolute paths as well. In this challenge, I used `/challenge/files/file_[bash]` as the absolute path argument for `/challenge/run`.

5. **Mixing Globs**  
   We can use different types of globbing together. After navigating to `/challenge/files`, I used `echo Look: *` (equivalent to `ls`) to list all available files. After observing that only `challenge`, `educational`, and `pwning` started with either `c`, `e`, or `p`, I provided `[cep]*` as an argument to `/challenge/run`.

6. **Exclusionary Globbing**  
   Using `!` or `^` with `[]` allows us to match files that do not contain the specified character. In this challenge, I used `[!pwn]*` as an argument to `/challenge/run`.
