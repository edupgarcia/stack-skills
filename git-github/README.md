# Git and GitHub

A repository for Git with Github courses from StackSkills.
This project does not intend to be a GIT user manual, but can be a good command reference.
The focus is to record what I've learned.

---

## Course 1 - Command Line Essentials: Git Bash for Windows

<https://stackskills.com/p/git-bash>

After installing Git for windows following course videos I started testing commands by opening Git-Bash.

1. List source/structure command shows contents os current or specified folder. The `-l` switch show more details about the files and the `-a` shows hidden files too.
    >`$ ls -l`

1. Which command search for executable files and show their current location.
    >`$ which git`

3. Move command is responsible for moving files/folders or just renaming them. The switch `-r` make it works recursivelly.
    >`$ mv <<origin>> <<destination>>`

4. Touch command creates empty files or change the timestamp of existing ones.
    >`$ touch <<filname>>`

5. Remove command deletes files/folders and in second case the `rmdir` can be used too. It also have `-r` to make recursive executions and also have `-f` which forces the execution.
    >`$ rm <<file>>`
    >`$ rm -rf <<folder>>`

6. Make dir command creates a folder and if you add `-p` switch (that stands for path) a folder/subfolder... structure is created.
    >`$ mkdir -p <<folder/subfolder/...>>`

7. Cat and Less commands are used to show contest of files and their main difference is that Cat show entire file at once and Less make breaks based in nomber of rows in the terminal window.
    >`$ cat <<file>>`
    >`$ less <<file>>`

8. Single bigger than (>) and double bigger than (>>) symbols are used to create files from commandd. Single one (>) overwrites existing file, on the other hand the Double one (>>) append to then end of it.
    >`$ ls -la > ls_la.txt`
    >`S ls -l >> ls_la.txt`


9. Change mode command - as the name says - *changes* the file attributes. In my example bellow it makes the file executable.
    >`$ chmod +x <<filename>>`


10. This one is not in the course but I wanted do add it due the fact I use it a lot. This command replaces a text by another in a file. The lower-case `s` means the search and the `g` means global.
    >`$ sed 's/OLD/NEW/g' <<source>>` **`>`** `<<target>>`

---

## Course 2 - Git Started with GitHub

<https://stackskills.com/p/git-started-with-github>

1. First of all shows the current Git version.
    >`$ git version`

2. In the sequence Git configuraton of global variables. Adding my user name and e-mail and after setup listed them.
    >`$ git config --global user.name "Eduardo Pereira Garcia"`
    >`$ git config --global user.email "edupgarcia.ti@gmail.com"`
    >`$ git config --global --list`

3. To download a copy of GitHub existing project. The `https://...` can be obtained directly from your project at **`github.com`**.
    >`$ git clone https://...`

4. Checking for any change is very simple, in the project folder type.
    >`$ git status`

5. For new/modifiled files staging process you can add usng `filename` or `.` to do all at once.
   >`$ git add <<filename>>`
   >`$git add .`

6. After staging it's necessary to commit the changes. Commiting makes changes effective and ready to be sent to the server. Adding a comment message using `-m` switch is always recommended once it makes easier what was changed in that specific commit.
    >`$ git commit -m "message"`

7. Finally as last step for this introduction course, the changes are stored at the server with the command below where `origin` repesents local version and `master` the branch at the server.
   >`$ git push origin master`


---

## Course 3 - Learning Git

<https://stackskills.com/p/learning-git2>

    UNDER CONSTRUCTION

## Course 4 - Mastering Git

<https://stackskills.com/p/mastering-git>

    UNDER CONSTRUCTION

---

## Extra - Python, MinGW 64 and Node.JS

During this learning adventure I needed to install additional software and as I used Windows 10 some software was required.
In Windows there are installer softwares where in Linux/MacOS you may have scripts to complete the actions.

### Python

I downloaded **Python 2.7** for Windows directly from its [website](https://www.python.org/downloads/windows/) and installed at **`C:\Python27`**.
After that I've made a setup to guarantee my git-bash has access to this version of Python.
As the file `~/.bash_profile` was automatically created in my `git-bash` by Git installation I just added required path reference but if it is not available for you, the change can be made in `~/.bashrc` or `~/.profile`.
   >`export PATH="$PATH:/c/Python27"`

### MinGW 64

I downloaded **MinGW 64** directly from its [website](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/) and installed at **`C:\mingw64`**.
Same as **Python** I made the change at `~/.bash_profile` now letting the changed line as below.
   >`export PATH="$PATH:/c/Python27:/c/mingw64:/c/mingw64/bin:/c/mingw64/lib"`

### Node.JS

I also downloaded **Node.JS** directly from its [website](https://nodejs.org/en/), I got lates **LTS** (Long Term Support) version and installed at default setup folder.
Together with it I installed all of its requirements though Powershell script executed automatically.

---
