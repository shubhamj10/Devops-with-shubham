# Linux Commands 



##  1. Basic File & Directory Commands

    `ls`
List files and directories.
 
 
    `clear`
Clear the terminal screen.


    `cd`
Change directory.


    `cp <source> <destination>`
Copy a file.

----

##  2. Viewing Files

    `cat <file>`
Show whole file content.

    `less <file>`
Scroll through file.

    `more <file>`
Older pager similar to less

    `head <file>`
Show first 10 lines.

    `head -n <number>`
Show first N lines.

    `tail <file>`
Show last 10 lines.

    `tail -n <number>`
Show last N lines.

    `tail -f <file>`
Follow live updates (logs).



---

##  3. Searching in Files (grep)

    `grep <word> <file>`
Case-sensitive search.

    `grep -i <word> <file>`
Case-insensitive search.


    `grep -i <word> *`
Search word inside every file in current folder.


    `grep -iR <word> *`
Recursive search in subdirectories.


    `grep -R <word> /path/*`
Recursive search inside a given directory.


     `grep -vi <word> <file>`
Show lines NOT containing the word.

---

##  4. Editing Files (Vim)

    `vim <file>`
Open file in Vim editor.


---

##  5. sed — Stream Editor (Find & Replace)

### Temporary replace (output only)
    * Replaces coronavirus with covid19 only in the output shown on the terminal.
    The file does NOT change because -i is not used.

    `sed 's/coronavirus/covid19/g' samplefile.txt`


### Permanent replace (`-i`)
    * Replaces all occurrences of covid19 with nothing inside the actual file.
    -i means the change is saved permanently.

    sed -i 's/covid19/nothing/g' samplefile.txt


---

##  6. cut Command — Extract Fields/Columns

### Extract usernames (1st field)

    cut -d: -f1 /etc/passwd


### Extract user IDs (3rd field)
    cut -d: -f3 /etc/passwd


---

## 7. awk — Advanced Text Processing

### Print first word of each line
    awk '{print $1}' /etc/passwd



---

##  8. System Configuration Files

### SELinux Config
