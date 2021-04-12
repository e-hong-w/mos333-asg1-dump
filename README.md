# EKT333 Modern Operating System  ![GitHub last commit](https://img.shields.io/github/last-commit/ehong-w/mos333-asg1-dump?style=for-the-badge)

In my own words,\
`Make your life easier in a blink of a Touch n Go scan!`

![forthebadge](https://forthebadge.com/images/badges/powered-by-electricity.svg)

---
### Assignment 1
![](https://img.shields.io/badge/score-16%2F20-brightgreen)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/ehong-w/mos333-asg1-dump)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/ehong-w/mos333-asg1-dump)
![GitHub all releases](https://img.shields.io/github/downloads/ehong-w/mos333-asg1-dump/total)

#### For this assignment you only need to submit answer to question 7. All the other question are basic necessities that one’s need to fruitfully answer question 7

#### Q7. The code below tries to implements multiprocess application. Analyze the code and answer the question that follows.

```
1. #include <stdio.h>
2. #include <stdlib.h>
3. #include <unistd.h>
4. #include <sys/types.h>
5. #include <sys/wait.h>
6. int main() {
7.    pid_t pid;
8.
9.
10.   printf("Child spawned, pid=%d ppid=%d \n",(int)<1>,(int)<2>);
11.   sleep(2);
12.   printf("Parent(%d) spawned child(%d)\n",(int)<3>,(int)<4> );
13.   sleep(2);
14.   return 0;
    }
```

&nbsp;&nbsp;&nbsp;&nbsp;a) Insert the code to create a child process at line 8 of the code in Figure 2 using the variable define at line 7.\
&nbsp;&nbsp;&nbsp;&nbsp;b) Beginning at line 9 insert the line(s) of code to check for the parent and child process created.\
&nbsp;&nbsp;&nbsp;&nbsp;c) Insert the code at line 10 in Figure 2 into the child process.\
&nbsp;&nbsp;&nbsp;&nbsp;d) Insert the code at line 12 in Figure 2 into the parent process.\
&nbsp;&nbsp;&nbsp;&nbsp;e) Specify the code that should be placed at item labeled <1>.\
&nbsp;&nbsp;&nbsp;&nbsp;f) Specify the code that should be placed at item labeled <2>.\
&nbsp;&nbsp;&nbsp;&nbsp;g) Specify the code that should be placed at item labeled <3>.\
&nbsp;&nbsp;&nbsp;&nbsp;h) Specify the code that should be placed at item labeled <4>.\
&nbsp;&nbsp;&nbsp;&nbsp;i) Edit the code that have been implemented from question 2a. until 2h. to force the parent process to wait for the child process.

---

#### Question A
```
pid = fork();
```
#### Question B
```
switch(pid)
{
  case -1:
    printf("Error");
    exit(-1);
  case 0:
    /*This is the child process.*/
    sleep(2);
    exit(0);
  default:
    /*This is the parent process.*/
    sleep(2);
}
```
#### Question C
```
switch(pid)
{
  case -1:
    printf("Error");
    exit(-1);
  case 0:
    printf("Child spawned, pid=%d ppid=%d \n", (int)<1>, (int)<2>);
    sleep(2);
    exit(0);
  default:
    /*This is the parent process.*/
    sleep(2);
}
```
#### Question D
```
switch(pid)
{
  case -1:
    printf("Error");
    exit(-1);
  case 0:
    printf("Child spawned, pid=%d ppid=%d \n", (int)<1>, (int)<2>);
    sleep(2);
    exit(0);
  default:
    printf("Parent(%d) spawned child(%d) \n", (int)<3>, (int)<4>);
    sleep(2);
}
```
#### Question E
```
getpid()
```
#### Question F
```
getppid()
```
#### Question G
```
getpid()
```
#### Question H
```
pid
```
#### Question I
```
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/wait.h>
int main()
{
  pid_t pid;
  pid = fork();
  switch(pid)
  {
    case -1:
      printf("Error");
      exit(-1);
    case 0:
      printf("Child spawned, pid=%d ppid=%d \n", (int)getpid(), (int)getppid());
      sleep(2);
      exit(0);
    default:
      printf("Parent(%d) spawned child(%d) \n", (int)getpid(), (int)pid);
      sleep(2);
      wait(NULL);
  }
  return 0;
}
```

---

**@blaco**🐏: How's life? Did you check out my [GitHub](https://github.com/ehong-w/)? 😟\
**@blaco**🐏: Drop me an email for other source code!\
**@blaco**🐏: It's not free, but it worths just a price of a lunch. 🥗

<p>
  <img width="512" src="https://user-images.githubusercontent.com/68590570/113911631-c52ca900-980c-11eb-8946-19ce84f84c40.png">
</p>


[![Making payment](https://media.giphy.com/media/vpTuttAlsmSOjEjLxo/source.mp4)](https://forms.gle/3e6AbU2eJQhvinUEA)


## 🧸 **Leave me a message?**
- 🍺 [E-mail](mailto:ehong.w@gmail.com?subject=[GitHub]%20Problem%20Description)
- 🧺 [Linkedin](https://www.linkedin.com/in/ehong-w/)
- ⛄ [Whatsapp]()
