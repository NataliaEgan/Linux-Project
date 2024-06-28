# Linux-Project
Using Linux commands to manage permissions
# Project description
Files permissions need to be updated within the projects directory. 
# Check file and directory details
First I used Linux commands to know what permissions were assigned to each department for a specific directory in the file system.
![image](https://github.com/NataliaEgan/Linux-Project/assets/173753740/ff6eff9f-bd63-4824-a221-9bc77251deb6)
I started by navigating to the projects directory then listing the contents and permissions the directory by entering the command ls -l. The results indicated that research_team is the owner of the files. I also checked if the projects directory contained any hidden files by entering the ls -la command, which revealed that there was one hidden file named .project_x.txt.
# Change file permissions
I started by determining whether any files have incorrect permissions and then changed the permissions as needed. 
![image](https://github.com/NataliaEgan/Linux-Project/assets/173753740/8a021401-a97f-4b89-8f11-2a002c9a555b)
I checked if any files in the projects directory have write permissions for the owner type of other by entering the ls -l command. The result showed that the project_k.txt file had write permissions for other users. I then changed the permissions of the file so other users don't have write permissions by entering the command chmod o-w project_k.txt. Since the file project_m.txt is a restricted file I change its permissions so the group doesn't have read or write permissions by enterring chmod g-r project_m.txt.
# Change file permissions on a hidden file
I determined if the hidden file had any incorrect permissions and then changed the permissions as needed.
![image](https://github.com/NataliaEgan/Linux-Project/assets/173753740/ac19730d-deb4-4f68-a650-8a46221a9860)
I started by checking the permissions of the hidden file .project_x.txt by enterring ls -la, which showed me that the user group owner types have incorrect permissions. I changed the permission of the file by enterring chmod u-w,g-w,g+r .project_x.txt
# Change directory permissions
I checked the group permissions of the /home/researcher2/projects/drafts directory and modified the permissions in a way that only researcher2 has access to the drafts directory and its contents.
![image](https://github.com/NataliaEgan/Linux-Project/assets/173753740/71d00d1a-8d99-4f67-8ee5-0c7850ef6cb0)
I consulted the permissions for the drafts directory by entering ls -l. This command showed me that the group has execute permissions granting it access to drafts. I removed the execute permission for the group from the drafts directory by enterring chmod g-x drafts.
