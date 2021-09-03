# My Project 1

## Setup:

1. remote into AWS instance and create user git and switch users to git

2. make directory .ssh and chmod 700 it

3. change directory into .ssh, create authorized_users file and chmod 600 

4. `mkdir failking` (to make command like URL command with creator in title)

5.  `nano .ssh/authorized_keys` and copy public key from ubuntu user over to this user.

6. change directory into `~/failking/` and `git init --bare repo`

7. create identity for ssh connection into the aws server inside `.ssh/config`

8. clone repo to my computer using `git clone git@awsgit:failking/awsRepo.git`

![successful clone screenshot](clonedNotSSH.PNG)