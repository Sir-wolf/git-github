# How use Git & Github ?
![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcamo.qiitausercontent.com%2F74f37adbe2cf302edd8b4a730a6498dbec7da459%2F68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f3132323134322f38303938303933392d303966612d613133332d353231342d6361356566653762393737332e706e67&f=1&nofb=1)

## Install Git & Global Setup

```bash
$ sudo apt-get install git 
$ git config --global user.name "YourNameHere"
$ git config --global user.email "YourEmailHere@xxxxx.xx"
```

## Example of Using

### Create a folder called "YourFolder"
```bash
$ mkdir YourFolder
```
### Initializes git
```bash
$ git init
```
### Create a hello.txt file, which contains "hello"
```bash
$ echo "hello" > hello.txt
```
### Looking at the status of git files
```bash
$ git status
```
![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi0.wp.com%2Fdiscoposse.com%2Fwp-content%2Fuploads%2F2016%2F11%2Fgit-status-add.png%3Fssl%3D1&f=1&nofb=1)
### We add hello.txt file to git queue
```bash
$ git add hello.txt
```
### We modify hello.txt file
```bash
$ echo "hello2!" > hello.txt
```
### Looking at the status of git files (he have changed)
```bash
$ git status
```
### We add Edited hello.txt file to git queue
```bash
$ git add hello.txt
```
### We do initial commit
```bash
$ git commit -m "Inirial commit"
```
### We looking logs
```bash
$ git log
```
### If you want delete git 
```bash
$ rm -rf .git/
```
### To see the difference between two modifications
```bash
$ git diff hello.txt
```
### Use branch 
```bash
$ git branch 
$ git checkout -b static-pages 
$ git branch 
$ git checkout master
$ git branch 
```

### Now we gonna generate a SSH key for upload to github
```bash
$ ssh-keygen -t rsa -b 4096 -C "YourEmailHere@xxxxx.xx"
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_rsa
$ sudo apt-get install xclip
$ ssh -T git@github.com
```
![](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Finfoheap.com%2Fwp-content%2Fuploads%2F2015%2F12%2Fgithub-ssh-add-key-interface.png&f=1&nofb=1)

### Now push git folder on github
```bash
$ git remote add origin https://github.com/xxxx/xxxxx.git
$ git push -u origin master
```
