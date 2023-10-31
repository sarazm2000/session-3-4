![20231031_214806](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/c9faad3b-efb9-4c03-8651-cd6872a7bbe1)---
name: فرم گزارش آزمایش سوم
about: برای نوشتن گزارش آزمایشگاه از این تمپلیت استفاده کنید
title: Session 3 Report
labels: documentation
assignees: amirhossein1376

---

Team Name: `98170849-98109729`

Student Name of member 1: `Sara Zahedi`
Student No. of member 1: `Paniz Halvachi`

Student Name of member 2: `98170849`
Student No. of member 2: `98109729`

- [ ] Read Session Contents.

### Section 3.3.1
- [ ] Investigate the /proc/ directory
    1. [ ] `[FILL HERE with an image of files in /proc/ directories. Use ls command.]`
    2. ![20231031_214806](https://github.com/Sharif-OS-Lab/session-3-4/assets/63396470/06a4ec67-533e-4a08-a8be-fd944206516d)


### Section 3.3.2

- [ ] Do 5 subtasks from 1 to 5:
    1. [ ] `[FILL HERE with the content of /proc/version. Use cat command.]`
    2. sara-paniz@98170849-98109729:/procs cat version
Linux version 5.4.0-125-generic (buildd@1cy02-amd64-083) (gcc version 9.4.0 (Ubuntu 9.4.0-1ubuntu1 20.04.1)) #141-Ubuntu SMP Wed Aug 10 13:42:03 UTC 2022
    1. [ ] `[FILL HERE with the content of two files with non-numeric name other thatn /proc/version.]`
    2. sara-paniz@98170849-98109729:/procs cat uptime
1399.19 179.27

First Value: Total number of seconds the system has been up since it was last booted
Second Value: Amount of time the system has been idle in seconds
       
    4. sara-paniz@98170849-98109729:/procs cat key-users
0:    67 66/66 52/1000000 1059/25000000
100:    1    1/1 1/200    9/20000
101:    1    1/1 1/200    9/20000
102:    1    1/1 1/200    9/20000
1000:    3    3/3 3/200    37/20000

First Value: Key type identifier.
Second Value: Number of keys of that type that are currently instantiated.
Third Value: Quota of keys of that type.
Fourth Value: Number of keys that have been created but not yet instantiated.
Fifth Value: Quota of keys that have been created but not yet instantiated.

    1. [ ] `[FILL HERE with the program you write for this part (see experiment guide for information).]`

```
#include <bits/stdc++.h>
using namespace std;

int main(){
    fstream file;
    file.open("/proc/version",ios::in);
    if(!file.is_open()){
        perror("error in reading");
        return 1;
    }
    fstream file2;
    file2.open("./Linux Version.txt",ios::out | ios::app);
    if(!file2.is_open()){
        perror("error in writing");
        return 1;
    }
    string line;
    while (!file.eof()){
        getline(file,line);
        file2 << line;
    }
return 0;
}
```
    
    1. [ ] `[FILL HERE with screen capture from your programs execution.]`
    1. [ ] `[FILL HERE with description about, what happens if you try to write a sentence in to /proc/version.]`

## Section 3.3.3

- [ ] Write (in English or Persian) about each file in /proc/(PID) directory:
    1. `[FILL HERE with description about cmdline]`
    1. `[FILL HERE with description about environ]`
    1. `[FILL HERE with description about stat]`
    1. `[FILL HERE with description about status]`
    1. `[FILL HERE with description about statm]`
    1. `[FILL HERE with description about cwd]`
    1. `[FILL HERE with description about exe]`
    1. `[FILL HERE with description about root]`

- [ ] Place your script for shwoing PID of running porcesses and their name here:
    - [ ] `[FILL HERE with your script]`

- [ ] Place your source code for a program that shows details of a program by receiving PID:
    - [ ] `[FILL HERE with your source code]`

### Section 3.3.4

- [ ] Write (in English or Persian) about each file in /proc/ directory:
    1. `[FILL HERE with description about meminfo]`
    1. `[FILL HERE with description about version]`
    1. `[FILL HERE with description about uptime]`
    1. `[FILL HERE with description about stat]`
    1. `[FILL HERE with description about mount]`
    1. `[FILL HERE with description about net directory (or file)]`
    1. `[FILL HERE with description about loadavg]`
    1. `[FILL HERE with description about interrupts]`
    1. `[FILL HERE with description about ioports]`
    1. `[FILL HERE with description about filesystem]`
    1. `[FILL HERE with description about cpuinfo]`
    1. `[FILL HERE with description about cmdline]`

- [ ] Place your source code for a program that shows details of processor:
    - [ ] `[FILL HERE with your source code]`

- [ ] Place your source code for a program that shows details of memory management sub-system:
    - [ ] `[FILL HERE with your source code]`

- [ ] Write your description about five important files at /proc/sys/kernel:
    - [ ] `[FILL HERE with your descript for 1st file]`
    - [ ] `[FILL HERE with your descript for 2nd file]`
    - [ ] `[FILL HERE with your descript for 3rd file]`
    - [ ] `[FILL HERE with your descript for 4th file]`
    - [ ] `[FILL HERE with your descript for 5th file]`

- [ ] Write your description about /proc/self file
    - [ ] `[FILL HERE with your description]`


## Source Code Submission

please submit all your codes in a zip file

 - [ ] `Zip File HERE`
