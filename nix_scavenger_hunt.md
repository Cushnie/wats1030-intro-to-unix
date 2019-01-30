# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* 
$ pwd
/c/Users/Colleen/Desktop/WATS3030/WEEK 02/wats1030-intro-to-unix

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
$ ls
challenge_files  
LICENSE  
nix_scavenger_hunt.md  
nix_scavenger_hunt_stretch.md  
README.md  
super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
$ ls -alh
total 74K
drwxr-xr-x 1 Colleen 197121    0 Jan 21 14:45 .
drwxr-xr-x 1 Colleen 197121    0 Jan 21 14:45 ..
drwxr-xr-x 1 Colleen 197121    0 Jan 21 14:45 .gitt                                                llenge_files
drwxr-xr-x 1 Colleen 197121    0 Jan 21 14:45 chaENSEllenge_files                                     _scavenger_hunt.md
-rw-r--r-- 1 Colleen 197121 1.1K Jan 21 14:45 LIC_scavenger_hunt_stretch.mdENSE                                             DME.md
-rw-r--r-- 1 Colleen 197121 5.7K Jan 21 16:01 nix_scavenger_hunt.md-rw-r--r-- 1 Colleen 197121  325 Jan 21 14:45 nix_scavenger_hunt_stretch.md
-rw-r--r-- 1 Colleen 197121 2.8K Jan 21 14:45 README.md-rw-r--r-- 1 Colleen 197121  268 Jan 21 14:45 super_scavengers.md

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
$ man 
man is the system's manual pager. Each page argument given  to  man  is normally  the  name of a program, utility or function.  The manual page associated with each of these arguments is then found and displayed.  A section,  if  provided, will direct man to look only in that section of the manual.
ls -a, --all
    do not ignore entries starting with .

ls -l
    use a long listing format

ls -h, --human-readable
    with -l, print sizes in human readable format (e.g., 1K 234M 2G)



* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
$ ls /
bin  
cmd  
dev  
etc  
git-bash.exe  
git-cmd.exe  
LICENSE.txt  
mingw64  
proc  
ReleaseNotes.html  
tmp  
unins000.dat  
unins000.exe  
unins000.msg  
usr


* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
Colleen@DESKTOP-C2H9GP5 MINGW64 /
$ pwd
/

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
$ pwd
/c/Users/Colleen

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
$ ls *.demo
2015_special_stuff.demo  cloaked-wookie.demo  scooter-double-mamba.demo

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
Colleen@DESKTOP-C2H9GP5 MINGW64 ~/desktop/wats3030/wats1030-intro-to-unix-master/challenge_files
$ cd ..

Colleen@DESKTOP-C2H9GP5 MINGW64 ~/desktop/wats3030/wats1030-intro-to-unix-master
$ pwd
/c/Users/Colleen/desktop/wats3030/wats1030-intro-to-unix-master


* Press the up arrow on your keyboard. *What just happened?*
$ pwd

* Press the up arrow a few more times. *What do you see?*
the commands used in reverse chron order

* Run the `history` command. *What do you see?*
$ history
    1  ls -al ~/.ssh
    2  git --version
    3  ssh-keygen -t rsa -b 4096 -C "cushniecolle@seattleu.edu"
    4  /c/Users/Colleen/.ssh/id_rsa
    5  /c/Users/Colleen/.ssh/id_rsa
    6  ls -al ~/.ssh
    7  ssh-keygen -t rsa -b 4096 -C "cushniecolle@seattleu.edu"
    8  eval $(ssh-agent -s)
    9  ssh-add ~/.ssh/id_rsa
   10  clip < ~/.ssh/id_rsa.pub
   11  clip < ~/.ssh/id_rsa.pub
   12  cat ~/ .ssh/id_rsa.pub
   13  git config --global user.name "Cushnie"
   14  git config --global user.email "cushniecolle@seattleu.edu"
   15  git config --global user.name
   16  git config --global user.email
   17  git@github.com:Cushnie/wats3010-intro-to-bootstrap-4.git
   18  git clone git@github.com:Cushnie/wats3010-intro-to-bootstrap-4.git
   19  code wats3010-intro-to-bootstrap-4/
   20  ping colleencushnie.com
   21  ls
   22  cd
   23  cd Documents
   24  cd
   25  cd ..
   26  cd
   27  ssh user@address
   28  pwd
   29  ls
   30  ls-alh
   31  'ls-alh'
   32  man
   33  cd /bin
   34  ls -l
   35  cd ~
   36  which scp
   37  pwd
   38  cat ~/.ssh
   39  cat ~/.ssh/id_rsa.pub
   40  ssh root@138.68.19.135
   41  sshe root@138.68.19.135
   42  ssh root@138.68.19.135
   43  ssh root@138.68.19.135
   44  pwd
   45  ls
   46  cd pictures/
   47  ls
   48  pwd
   49  scp JudgeJudy.jpg root@138.68.19.135:~wats-1030-moving-files/challenge_files/img/
   50  ls
   51  scp JudgeJudy.jpg root@138.68.19.135:~wats1030-moving-files/challenge_files/img/
   52  scp JudgeJudy.jpg root@138.68.19.135:~/wats1030-moving-files/challenge_files/img/
   53  pwd
   54  ls
   55  ls -alh
   56  man -C file
   57  cd ..
   58  ls
   59  cd wats1030-intro-to-unix
   60  ls
   61  cd license
   62  cd challenge_fiels
   63  cd challenge_files
   64  ls
   65  man
   66  cd ..
   67  whereis man
   68  whereis
   69  ls
   70  challenge_files
   71  cd challenge_files
   72  ls
   73  man
   74  cd tmp
   75  man
   76  ls
   77  cd ..
   78  ls
   79  cd test2
   80  ls
   81  man
   82  cd ..
   83  ls
   84  cd wow
   85  ls
   86  cd ..
   87  cd ..
   88  --human-readable
   89                with -l, print sizes in human readable format (e.g., 1K 234M 2G)
   90  cd ..
   91  pwd
   92  cd ..
   93  /
   94  ls
   95  pwd
   96  ls
   97  cd 'week 02'
   98  ls
   99  cd wats1030-intro-to-unix
  100  ls
  101  cd /
  102  pwd
  103  ~
  104  cd ~
  105  pwd
  106  ls
  107  cd desktop
  108  ls
  109  cd wats3030/~
  110  cd wats3030/
  111  ls
  112  cd wats1030-intro-to-unix-masater
  113  cd wats1030-intro-to-unix-master
  114  ls
  115  cd challenge_files
  116  ls
  117  ~.demo
  118  ls *.demo
  119  cd ..
  120* pwd
  121  ~.demo
  122  history
  history of commands executed in this environment

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
Colleen

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
No one else. (thank goodness ... I live alone LOL)

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
$ uptime
bash: uptime: command not found
uptime gives a one line display of the following information.  The current time, how long the system has been running,  how  many  users  are currently  logged  on,  and the system load averages for the past 1, 5, and 15 minutes.

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
$ ps aux
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     1588       1    1588       1588  cons0     197609 19:55:15 /usr/bin/bash
     2316   10400    2316      11452  pty0      197609 17:15:31 /usr/bin/bash
    15072    1588   15072      10608  cons0     197609 21:32:28 /usr/bin/ps
    10400       1   10400      10400  ?         197609 17:15:30 /usr/bin/mintty
ps displays information about a selection of the active processes.  If you want a repetitive update of the selection and the displayed information, use top(1) instead.

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
The  top  program  provides  a dynamic real-time view of a running system.  It can display system summary information as  well  as  a
       list  of processes or threads currently being managed by the Linux kernel.  The types of system summary  information  shown  and  the types,  order  and size of information displayed for processes are all user configurable and that configuration can be  made  persistent across restarts.
       
### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
