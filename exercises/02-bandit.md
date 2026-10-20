# Bandit Levels 0-10 Runbook

- **Level 0 → Level 1**: `ssh bandit0@bandit.labs.overthewire.org -p 2220` followed by `cat readme`
- **Level 1 → Level 2**: `ssh bandit1@bandit.labs.overthewire.org -p 2220` followed by `cat ./-`[cite: 3]
- **Level 2 → Level 3**: `ssh bandit2@bandit.labs.overthewire.org -p 2220` followed by `cat "spaces in this filename"`
- **Level 3 → Level 4**: `ssh bandit3@bandit.labs.overthewire.org -p 2220` followed by `cd inhere`, `ls -la`, and `cat .hidden`
- **Level 4 → Level 5**: `ssh bandit4@bandit.labs.overthewire.org -p 2220` followed by `cd inhere`, `file ./*`, and `cat ./file07`
- **Level 5 → Level 6**: `ssh bandit5@bandit.labs.overthewire.org -p 2220` followed by `find . -type f -size 1033c ! -executable` and `cat ./inhere/maybehere07/.file2`
- **Level 6 → Level 7**: `ssh bandit6@bandit.labs.overthewire.org -p 2220` followed by `find / -user bandit7 -group bandit6 -size 33c 2>/dev/null` and `cat /var/lib/dpkg/info/bandit7.password`
- **Level 7 → Level 8**: `ssh bandit7@bandit.labs.overthewire.org -p 2220` followed by `grep "millionth" data.txt`
- **Level 8 → Level 9**: `ssh bandit8@bandit.labs.overthewire.org -p 2220` followed by `sort data.txt | uniq -u`
- **Level 9 → Level 10**: `ssh bandit9@bandit.labs.overthewire.org -p 2220` followed by `strings data.txt | grep '===='`
