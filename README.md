![image](https://github.com/user-attachments/assets/5b48bd14-f375-4cab-9258-068a837627e0)## Виконав самостійно Шевченко Артем РПЗ-23А
# Laboratory Work Report № 10
## Topic: "Changing File Owners and Access Rights in Linux. Special Directories and Files in Linux"

### Objective of the Work:
- To acquire practical skills in working with the Bash command line.
- To familiarize with basic actions for changing file ownership and access rights.
- To learn about special directories and files in Linux.

### Glossary of Terms
- **File Ownership**: The user and group that own a file.
- **Permissions**: Rights assigned to users and groups regarding file access.
- **UID (User  ID)**: A unique identifier for a user.
- **GID (Group ID)**: A unique identifier for a group.
- **setuid**: A permission that allows a user to run an executable with the permissions of the file owner.
- **setgid**: A permission that allows a user to run an executable with the permissions of the group owner.
- **Sticky Bit**: A permission that allows only the file owner to delete or modify the file in a directory.

### Answers to Preliminary Preparation Tasks
1. **What is the purpose of the `id` command?**
   - The `id` command displays the user ID (UID) and group ID (GID) of the current user, along with the groups the user belongs to.

2. **How to view the access rights of a file owner?**
   - You can view the access rights of a file owner using the `ls -l filename` command.

3. **How to change the group owner?**
   - You can change the group owner using the `chgrp group_name filename` command.

4. **How to check the type of the current file in the terminal? Provide examples for different file types.**
   - You can check the type of a file using the `file filename` command. For example:
     - `file script.sh` (returns "Bourne-Again shell script")
     - `file image.png` (returns "PNG image data")

5. **What are the uses of setuid and setgid permissions?**
   - `setuid` allows users to execute a file with the permissions of the file owner, which is useful for programs that require elevated privileges. `setgid` allows users to execute a file with the permissions of the group owner, facilitating group collaboration.

6. **What is the purpose of the sticky bit? Provide examples of when this permission is appropriate.**
   - The sticky bit is used on directories to ensure that only the file owner can delete or rename files within that directory. It is commonly used in shared directories like `/tmp`.

### Work Progress
1. **Initial Work in CLI Mode in Linux OS:**
   - Start the Linux Ubuntu operating system and open the terminal.
   - Execute all command examples presented in the NDG Linux Essentials labs: Lab 17: Ownership and Permissions and Lab 18: Special Directories and Files.

2. **Command Table:**

| Command Name | Purpose and Functionality |
|--------------|---------------------------|
| `id`         | Displays user and group IDs. |
| `ls -l`      | Lists files with detailed permissions. |
| `chown`      | Changes file owner. |
| `chgrp`      | Changes file group owner. |
| `chmod`      | Changes file permissions. |
| `newgrp`     | Changes the current primary group. |
| `file`       | Determines the type of a file. |

### Practical Tasks in the Terminal
1. **Create three new users.**                                                                                                                                                                                                                                                                  ![image](https://github.com/user-attachments/assets/648d27d3-a1ed-4e84-aa76-c4de1285f8f1)


2. **Create a new user group and add two of the three created users.**                                                                                                                                                                                                                          ![image](https://github.com/user-attachments/assets/a0be37aa-35ac-4427-b706-c8fd4bb0c1ab)


3. **Create a new file accessible for reading, editing, and executing by the file owner.**                                                                                                                                                                                                      ![image](https://github.com/user-attachments/assets/fa508b81-65e5-43bd-8aad-47b37a926da4)


4. **Grant read and execute permissions to the group owner without edit permissions.**                                                                                                                                                                                                         ![image](https://github.com/user-attachments/assets/f2e81ff6-5a5e-4969-8a1c-8c4fe2dae349)


5. **Deny access to other users.**Denying access to other users (already done in the previous point via chmod 750)                                                                                                                                                                                 Denying access to other users (already done in the previous point via chmod 750)

6. **Create directories with specified access rights.**                                                                                                                                                                                                                                          ![image](https://github.com/user-attachments/assets/9b917436-9178-498f-92ca-482dc2b48aa1)


7. **Create an empty file named `emptyfile` and modify its permissions.**                                                                                                                                                                                                                       ![image](https://github.com/user-attachments/assets/e2274b74-34d9-425c-bbcb-d46b9f7d2c84)


8. **Create a directory where all files automatically belong to your user group.**                                                                                                                                                                                                              ![image](https://github.com/user-attachments/assets/f775ff4f-1903-47ef-894d-fa29322bfd72)      
9. **Create hard and symbolic links for files.**
10. **Test file access and deletion by other users.**

### Control Questions
1. **Provide examples of changing access rights using the symbolic method.**
   - `chmod u+x file` (adds execute permission for the user).
   - `chmod g-w file` (removes write permission for the group).

2. **Provide examples of changing access rights using the numeric method.**
   - `chmod 755 file` (sets read, write, and execute for owner, and read and execute for group and others).

3. **What is the purpose of the `umask` command?**
   - The `umask` command sets default permissions for newly created files and directories.

4. **Compare hard and symbolic links.**
   - Hard links point to the same inode and cannot span different filesystems, while symbolic links are pointers to file names and can span filesystems.

5. **Can a file be executed if it has execute permissions but no read permissions?**
   - No, a file cannot be executed without read permissions because the system needs to read the file's content to execute it.

6. **If we change access rights in the current session, will they be saved in the next session?**
   - No, changes made in a session are temporary unless explicitly saved.

7. **Is there a template that the system uses for permissions when creating new files? How can default permissions be changed?**
   - Yes, the system uses the `umask` value to determine default permissions. You can change it using the `umask` command.

8. **How to create a hard link? When is it appropriate to use?**
   - Use `ln original_file hard_link`. Hard links are useful for backup purposes.

9. **How to create a symbolic link? When is it appropriate to use?**
   - Use `ln -s original_file symbolic_link`. Symbolic links are useful for linking to files across different filesystems.

10. **What is the correct directory for creating a temporary file that will not be needed after the program closes?**
    - The `/tmp` directory is appropriate for temporary files.

11. **What happens to the other files if the original file is deleted?**
    - If the original file is deleted, the hard link remains functional, while the symbolic link becomes broken.

### Conclusion
In this laboratory work, we explored the concepts of file ownership, permissions, and special directories in Linux. We gained practical experience in using various commands to manage file access rights and learned about the implications of special permissions like `setuid`, `setgid`, and the sticky bit. The exercises provided a comprehensive understanding of how to effectively manage files and directories in a multi-user environment.
