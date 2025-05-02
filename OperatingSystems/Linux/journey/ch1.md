# Chapter 1: Basic Commands and Directory Hierarchy

The exercises are from the following topics:
- Basic navigation
- File and directory manipulation
- Viewing file content
- Searching and filtering
- Understanding permissions
- Working with commands and help systems

---

### 🔍 Filesystem Navigation & Inspection

**1. Map Your Filesystem:** Use `tree`, `ls`, `cd`, and `pwd` to draw (on paper or a text file) a hierarchy map of your home directory and `/etc`.

**2. Breadcrumb Trail:** Navigate deep into `/usr`, then use `pwd` to echo your current path. Exit back step-by-step using `cd ..` only.

**3. Hidden Treasures:** List all hidden files in your home directory. What do `.bashrc` and `.profile` do?

**4. Find Me If You Can:** Use `find` to search for all `.conf` files under `/etc` (e.g., `find /etc -name "*.conf"`). Count them.

### 📁 File & Directory Operations

**5. Directory Lab:** Create a directory structure: `projects/linux/basics/{scripts,notes,logs}` using one command.

**6. Log the Logs:** Use `touch` to create 5 fake log files named `log1.log`, `log2.log`... etc., in the `logs` folder.

**7. Bulk Renamer:** Rename all `.log` files to `.txt` using a `for` loop.

**8. Copycat:** Copy `/etc/hosts` and `/etc/resolv.conf` into your notes folder. Don’t overwrite existing ones.

**9. Clean Sweep:** Delete all `.txt` files in logs, but only after confirming their count.

### 📄 File Content & Redirection

**10. Who’s Talking?** Use `echo` to write a sentence to a file called `hello.txt`, then view it with `cat`, `less`, and `head`.

**11. Copy & Compare:** Duplicate a file and use `diff` to show they’re the same. Modify the copy slightly and compare again.

**12. Combiner:** Create 3 small `.txt` files with different content. Use `cat` to combine them into a new file.

**13. Line Count Challenge:** Create a file with 20 lines. Use `wc`, `head`, and `tail` to count and extract specific lines.

**14.Output Redirect Mastery:** Use `>` to write and `>>` to append to a file. Create a log tracking what you learn each day.

### 🔧 Process, Help, and History

**15. Man Page Explorer:** Read the `man` page for `ls`, `grep`, `find`, and `bash`. Summarize one cool option for each.

**16. Reverse Search Detective:** Use `reverse-i-search (Ctrl+R)` to find a command you ran earlier. Re-run it.

**17. Your Command Diary:** Use `history` to see your command list. Filter it using `grep` for commands like `cd`, `mkdir`, etc.

**18. Get Me Help Fast:** Use `--help` and `man` to learn the difference between `ls --help` and `man ls`.

### 🔐 Permissions & Ownership

**19. Permission Puzzle:** Create a file, set its permission to `rw-r--r--`, then try editing it as another user (if possible).

**20. Secret Folder:** Create a folder, set permissions so only you can access it. Confirm with `ls -ld`.

**21. Chameleon Files:** Change a file’s ownership (if using `sudo` or `root`), then verify with `ls -l`.

**22. Octal Workout:** Practice setting permissions using numeric (e.g., `chmod 755`) and symbolic (`chmod u+x`) modes.

### 🧩 Bonus Challenges

**23. Command Pipeline:** Combine `ps`, `grep`, and `wc` to count how many times a particular process is running.

**24. Temporary Playground:** Create a `/tmp/mytest` directory, do experiments there, and delete it cleanly afterward.

**25. Simulate a Log Monitor:** Use `tail -f` on `/var/log/syslog` (or `/var/log/messages`) to watch logs update in real time.

**26. Directory Report Generator:** Write a one-liner to list the number of files and total disk usage of every directory in your `home`.