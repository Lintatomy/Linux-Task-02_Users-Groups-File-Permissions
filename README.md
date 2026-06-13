# Linux-Task-02_-Users-Groups-File-Permissions

The aim of this activity is to learn and practice user and group management in Linux, ownership management of files, and permission management of files. By performing activities related to Linux, the students will learn how to create users and groups, assign file ownership, manage file access control using chmod and chown command, and analyze permission management. Additionally, through this activity, important concepts such as Access Control and Principle of Least Privilege can be learned.

Part A: Understanding Users :-

Commands
whoami
id
cat /etc/passwd

Answers
1. What is your current username?
The username of the currently logged-in user.

2. What is UID?
UID (User ID) is a unique numerical identifier assigned to each user in Linux.

3. What is GID?
GID (Group ID) is a unique numerical identifier assigned to a group.

4. What information does /etc/passwd contain?
Username
User ID (UID)
Group ID (GID)
Home directory
Login shell
User description/comment

Screenshort
<img width="1280" height="800" alt="screenshot1" src="https://github.com/user-attachments/assets/65a65a04-60a6-459c-bce5-f60a2da8109e" />

Part B - Create Users & Groups :-

Groups Created:
interns
cyberteam

Users Created:
student1
student2
student3

Verification Commands:
groups student1
groups student2
groups student3

id student1
id student2
id student3

Screenshort
<img width="1280" height="800" alt="screenshot2" src="https://github.com/user-attachments/assets/90826cd8-cfc0-4fb2-a03d-74ab727538ae" />

Part C - File Ownership :-

Folder Created:
CyberSecurity_Project

Files Created:
report.txt
notes.txt
credentials.txt

Ownership Changed:
sudo chown student1 report.txt
Ownership Information
| Item           | Details                          |
| -------------- | -------------------------------- |
| Original Owner | kali                             |
| New Owner      | student1                         |
| Command Used   | `sudo chown student1 report.txt` |

Screenshort
<img width="838" height="609" alt="screenshot5" src="https://github.com/user-attachments/assets/2f8b95b3-e293-446d-b264-87032a3b5195" />

Part D - File Permissions

File Created:
security_policy.txt

Permissions Tested:
Read Only
chmod 444 security_policy.txt
Result:
-r--r--r--

Read & Write
chmod 664 security_policy.txt
Result:
-rw-rw-r--

Full Access
chmod 777 security_policy.txt
Result:
-rwxrwxrwx

Screenshort
<img width="1043" height="522" alt="screenshot6" src="https://github.com/user-attachments/assets/02a59fea-e5cd-4d0a-82cf-80e53618e40b" />

Part E - Permission Analysis :-

1. Permission: 755
Representation:
rwxr-xr-x
Owner Rights:
Read, Write, Execute
Group Rights:
Read, Execute
Others Rights:
Read, Execute
Use Case: 
Executable programs, web server directories.

2. Permission: 644
Representation:
rw-r--r--
Owner Rights:
Read, Write
Group Rights:
Read
Others Rights:
Read
Use Case:
Normal text files and configuration files.

3. Permission: 777
Representation:
rwxrwxrwx
Owner Rights:
Read, Write, Execute
Group Rights:
Read, Write, Execute
Others Rights:
Read, Write, Execute
Use Case:
Generally not recommended due to security risks.

4. Permission: 600
Representation:
rw-------
Owner Rights:
Read, Write
Group Rights:
No Access
Others Rights:
No Access
Use Case:
Password files, private documents.

5. Permission: 700
Representation:
rwx------
Owner Rights:
Read, Write, Execute
Group Rights:
No Access
Others Rights:
No Access
Use Case:
Private scripts and personal directories.

Detailed analysis available in  Permission Analysis.txt

Part F: Security Challenge :-

| File                | Recommended Permission | Reason                           |
| ------------------- | ---------------------- | -------------------------------- |
| password_backup.txt | 600                    | Contains sensitive passwords     |
| public_notice.txt   | 644                    | Everyone can read it             |
| system_log.txt      | 640                    | Admin can modify, others limited |
| personal_notes.txt  | 600                    | Private information              |

Explanation
password_backup.txt
Contains confidential information.
Only owner should access it.
public_notice.txt
Public information.
Everyone can read.
system_log.txt
Logs should not be modified by ordinary users.
Only administrators should write.
personal_notes.txt
Personal data should remain private.

Part G: Linux Security Research :-

1. Explain the significance of file permission
File permissions determine the accessibility level of files by users. They ensure the protection of sensitive data from any unauthorized person accessing it.

2. What are the possible consequences of granting 777 permission on sensitive data?
It is open to any action from reading to deleting it. This may result in:
Data theft
Tampering with data
Malware insertion
Harm to the system

4. What is the Principle of Least Privilege?
According to the principle of least privilege, users should have access to the minimal amount of permissions that they need to undertake certain activities.

5. Why do companies deny their employees permission?
This is due to the following reasons:
Sensitive data protection
Prevention of accidental changes
Insider threat mitigation

Folder Structure:-
Linux_Task_02_StephenJ/
│
├── Screenshots/
│   ├── S1_whoami.png
│   ├── S1_id.png
│   ├── S1_passwd.png
│   ├── S2_groups.png
│   ├── S2_users.png
│   ├── S3_ownership_before.png
│   ├── S3_ownership_after.png
│   ├── S4_readonly.png
│   ├── S4_readwrite.png
│   └── S5_fullaccess.png
│
├── Commands Used.txt
├── Permission Analysis.txt
├── Security Challenges.txt
├── Linux Security Research.txt
└── README.md
