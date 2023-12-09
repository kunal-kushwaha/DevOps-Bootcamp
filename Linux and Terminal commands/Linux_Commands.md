-----LINUX COMMANDS-----

1. ls (list)
list all the things in the folder
a.  ls -a
    shows hidden files 
    any file starting with '.' is hidden 
b.  ls -R
    shows the content of the sub-directories also

2. mkdir (make directory)
make a new directory
a.  mkdir -p first/second/third/fourth
   creates a series of directories inside first

3. cd (change directory)
it is used to change current working directory
for eg
cd second (as second is inside first)
a.  cd ..
   move to parent directory
b.  cd second/third/fourth
   move inside multiple directories

4. echo
display
a.  echo "hello world" > file.txt
    override the content of file.txt with hello world

Environment Variables - These are named values that are used to change how the commands, processes etc are executed

Path Environment Variables - When you write any command, terminal is going to check in $PATH, else return command not found
for eg:
python3
echo
git

echo $PATH
/c/Users/DELL/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/DELL/bin:
/c/ProgramData/Oracle/Java/javapath:/c/Program Files/Common Files/Oracle/Java/javapath:/c/Windows/system32:
/c/Windows:/c/Windows/System32/Wbem:/c/Windows/System32/WindowsPowerShell/v1.0:/c/Windows/System32/OpenSSH:
/c/Program Files/NVIDIA Corporation/NVIDIA NvDLISR:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:
/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/MinGW/bin:/cmd:/c/Program Files/dotnet:
/c/Program Files/nodejs:/c/ProgramData/chocolatey/bin:/c/Users/DELL/AppData/Local/Microsoft/WindowsApps:
/c/Program Files/JetBrains/IntelliJ IDEA 2021.3.1/bin:/c/Program Files/JetBrains/IntelliJ IDEA Community Edition 2021.3.1/bin:
/c/Users/DELL/AppData/Local/Programs/Microsoft VS Code/bin:/c/Program Files/Multipass/bin:/c/Users/DELL/Documents/flutter/bin:
/c/Users/DELL/AppData/Roaming/npm:/c/Users/DELL/AppData/Local/atom/bin:/usr/bin/vendor_perl:/usr/bin/core_perl
(here env var are separated by ':')

5. cat (concatenate)
a.  cat > hello
    creates a file named hello in the current working directory
    now everything you type will be in that file
    to exit out of hello, use Ctrl + C
   
    '>' 
    redirect the output
b.  cat file.txt two.txt
    merges output and prints
c.  cat file.txt two.txt > total.txt
    merge contents of file.txt and two.txt in total.txt
d.  cat file.txt | tr a-z A-Z > upper.txt
   
    '|' 
    output of the first command acts as an input for the second command
e.  cat file.txt \
    adds new command in a new line

6. tr (translate)

7. pwd (present working directory)

8. touch
creates a new file
   
    Q diff b/w touch & cat?
    cat command: It is used to create the file with content.
    touch command: It is used to create a file without any content.

9. cp (copy)
i.  two file names
    cp first.txt second.txt
    copies the content of first file to second file
ii. more than 2 file names
    cp first.txt second.txt third.txt fourth.txt
    copies the content of first, second & third file to fourth file
    or in other words it copies the contents of all files except last file to the last file  

10. mv (move)
i.  used to rename a file or folder. 
    (this works if 2nd file in command ie second.txt does not exist)
    mv first.txt second.txt
    renames first.txt to second.txt

ii. used to move contents of one file to a different file.
    (works if 2nd file in command ie second.txt exists)
    mv first.txt second.txt
    overwrites the contents of first.txt in second.txt & deletes initial first.txt file 

11. rm (remove)
used to remove a file or folder

12. sudo (Super User DO)
execute a command as an administrative user and it requires password

13. df (disk free) 
check system's disk space usage
a.  df -m
    shows disk space in mb

14. du (disk usage)
shows disk usage statistics of current dir

15. head
view first 10 lines of file
a.  head total.txt
    first 10 lines
b.  head n 4 total.txt
    first 4 lines

16. tail
view last 10 lines of file
a.  tail total.txt
    last 10 lines
b.  tail n 4 total.txt
    last 4 lines

17. diff
helps in comparing the data between two files line by line and when 
any difference is found between the files then the differences will 
also be displayed along with the line numbers

18. locate
helps in finding files
a.  locate "*.txt"
    search for all files with txt extension

19. find
finds files & folders

a.  find . -type d
    finds only folders
b.  find . -type f
    finds only files
c.  find . -type f -name "two*"(replace -name with -iname for case sensitive searches)
    finds for all files starting with two
d.  find . -maxdepth 2
    all files only 2 folder inside or less
e.  find . -size +1k
    size more than 1 kb
f.  find . -empty
    finds all empty files & folders
g.  find . type -f name "*.txt" -exec rm -rf {} +
    deletes all txt files of that dir

---permissions---
ls -l hello.txt (-check perms)
-rw-r--r-- 1 DELL 197121 0 Apr 11 15:02 hello.txt

here 1st one is for user 2nd for group 3rd for others
r read
w write
x execute

20. chmod (change mode)
used to change perms
a.  chmod u=rwx,r=rx,o=r
    ls -l hello.txt
    -rwxr-xr-- 1 DELL 197121 0 Apr 11 15:02 hello.txt
b.  (using numbers)
    4 read
    2 write
    1 execute
    user,group,other
    for eg to read & execute use 4+1=5
    
    chmod 754
    ls -l hello.txt
    -rwxr-xr-- 1 DELL 197121 0 Apr 11 15:02 hello.txt

21. whoami
displays username of current user

22. chown (change owner)
 
23. grep (Global Regular Expression Print)
used to search for text within our files (case sensitive)

a.  grep -w "school" hello.txt
    searches for particular word  
b.  grep "school" hello.txt 
    searches for text in any word
c.  grep -iw "school" hello.txt
    case sensitive and a word
d.  grep -n "school" hello.txt
    shows line number
e.  grep -r "school" hello.txt
    search recursively ie folders inside folders
f.  grep -win "school" hello.txt
    word, case sensitive and shows line number
g.  grep -win "school" ./*.txt
    searches for word in current dir

24. history
used to display the history of the commands executed by the user
a.  history | grep "ls"
    shows history of all commands that were ls commands

24. sort 
used to sort contents of a text file, line by line
a.  sort -r hello.txt
    sorts in reverse order
b.  sort -f hello.txt
    case insensitive sorting
c.  sort -n hello.txt
    sorts file with numeric data present inside

25. jobs 
jobs are processes started by the shell
display current jobs that are running

26. ping (Packet INternet Groper)
used to check the network connectivity between host and server/host

27. top
displays the running processes on the system

28. kill
used to terminate processes manually

29. uname
it gives information about your linux system
a.  uname -o
    displays the type of system
b.  uname -m
    displays the architecture 
c.  uname -r
    displays the kernel version

30. zip 
zip files 

31. unzip 
unzip files

32. hostname
used to obtain the DNS name and set the system’s hostname or NIS

33. useradd
used to add user accounts to your system

34. userdel
used to delete a user account and related files

35. lscpu
get cpu details

36. free
check free memory

37. vmstat (Virtual Memory Stats)
displays virtual memory stats
a.  vmstat -S m
    displays stats in mbs

38. id
used to find out user and group names and numeric ID’s

39. getent
helps the user to get the entries in a number of important text files

40. lsof (List Of Open File)
displays list of files that are opened 

41. nslookup (Name Server Lookup)
used to get information from the DNS server

42. netstat
displays all the active ports

43. sed (Stream EDitor)

44. cut
cut out selected portions of each line of a folder
a.  cut -c 1-2 hello.txt
    display first two columns of the file
