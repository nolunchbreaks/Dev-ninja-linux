# Dev-ninja-linux admin
- sudo - i
- Create users and passwd
- useradd user1
- passwd user1
- useradd user2
- passwd user2
- useradd user3
- passwd user3
- create groups- devops, aws
- groupadd devops
- groupadd aws
- change primary groups of user2, user3 to devops group
- usermod -g devops user2
- usermod -g devops user3
- add aws group as a secondary group to user1
- usermod -aG aws user1
- create the file and directory structure as shown in the diagram
- #!/bin/bash

# Create root-level directories
- mkdir -p home/dir1 home/dir2/dir1/dir2/dir10 home/dir3/dir11 home/dir4/dir12 home/dir5/dir13
- mkdir -p dir6/dir10 dir7 dir8/dir9 opt/dir14/dir10

# Create files in the specified directories
- touch home/dir1/f1 home/dir2/dir1/dir2/f3 home/dir4/dir12/f5 home/dir5/dir13/f4
- touch dir7/f3 dir8/f1 dir8/f2 opt/dir14/dir10/f3
- echo "Directories and files have been created!"
- change group of dir1/ dir7/dir10, /f2 to devops group
- chgrp devops /dir1
- chgrp devops /dir7/dir10
- chgrp devops /f2
- change ownership of /dir1. /dir7/dir10, /f2 to user1
- chown user1 /dir1
- chown user1 /dir7/dir10
- chown user1 /f2
- login as user1
- su -user1
- create users and set passswd user4, user5
- useradd user4
- passwd user4
- useradd user5
- passwd user5
- create groups -app, dataabase
- groupadd app
- groupadd database
- switch to user4
- su-user4
- create directory -/dir6/dir4
- mkdir -p /dir6/dir4
- create file -/fr
- touch /f3
- move file from
- mv /dir1/f1 /dir2/dir1/dir2
- rename the file /f2 to f4
- mv /f2 /f4
- login as user1
- su -user1
- create directory -/home/user2/dir1
- mkdir -p /home/user2/dir1
- Change to “/dir2/dir1/dir2/dir10” directory and create file “/opt/dir14/dir10/f1” using relative path
- cd /dir2/dir1/dir2/dir10
- touch ../../../../opt/dir14/dir10/f1
- Move the file from “/opt/dir14/dir10/f1” to user1 home directory
- mv /opt/dir14/dir10/f1 ~/
- Delete the directory recursively “/dir4
- rm -rf /dir4
- Delete all child files and directories under “/opt/dir14”
- rm -rf /opt/dir14/*
- Write text to /f3
-echo "Linux assessment for a DevOps Engineer!! Learn with Fun!!" > /f3
