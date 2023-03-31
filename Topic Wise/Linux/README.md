

### Users and Groups

- /etc/passwd contains the data related to the users on the system
- group lets you give permissions to a user or users
	- /etc/group contains the details of the groups on the system

```bash
adduser <user> # to add a user
userdel <user> # to delete a user
passwd <user> # to change the password


groupadd <group_name>
groupdel <group_name>
adduser <user_name> <group_name>
deluser <username> <group_name>


chown <user_name> <file_name> # to change the user owner of the file
chgrp <group_name> <file_name> # to change the group owner of the file

```


- permissions
	- 777
	- user - group - others
	- user permission is for the owner of the file
	- group permission is for the groups that own the file




## Configuratioin
- Zsh configuraiton
	- [zsh: Syntax Highlighting, vi-mode, Autocomplete, more - YouTube](https://www.youtube.com/watch?v=eLEo4OQ-cuQ)
- 