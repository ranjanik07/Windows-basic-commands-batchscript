# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file
Save each script in a file with a .bat extension.
Ensure you have the necessary permissions to perform the operations.
Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "MyLab" on the desktop.

```
C:\Users\admin>mkdir Mylab
C:\Users\admin>cd Mylab
```

![image](https://github.com/user-attachments/assets/2e01c194-c40c-4019-afbc-943a29bd5508)


## COMMAND AND OUTPUT

Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.
```
C:\Users\admin\Mylab>echo > MyFile.txt
```
![image](https://github.com/user-attachments/assets/12d9c1f3-82b2-40f7-974e-a58856ae27e7)


## COMMAND AND OUTPUT

List the contents of the "MyLab" directory.
```
C:\Users\admin\Mylab>dir
```
![image](https://github.com/user-attachments/assets/3f3ca3a1-f96e-46a3-9f8c-f8e0af3e156d)


## COMMAND AND OUTPUT

Copy "MyFile.txt" to a new folder named "Backup" on the desktop.
```
copy "Mylab\MyFile.txt" "Backup\copy.txt"
```
![image](https://github.com/user-attachments/assets/370a127e-4c14-4006-a167-a18de4337b19)


## COMMAND AND OUTPUT

Move the "MyLab" directory to the "Documents" folder.
```
move "Mylab\*.*" "Backup"
```
![image](https://github.com/user-attachments/assets/5a940dfc-3400-44ec-b4a3-1e68349eb0c5)


## COMMAND AND OUTPUT


## Exercise 2: Advanced Batch Scripting
Create a batch script named "BackupScript.bat" that creates a backup of files with the ".docx" extension from the "Documents" folder to a new folder named "DocBackup" on the desktop.
```
@echo off
REM BackupScript.bat - Copies all .docx files from Documents to Desktop\DocBackup

REM Define source and destination paths
set "source=%USERPROFILE%\C:\User\admin\Mylab"
set "destination=%USERPROFILE%\C:\User\admin\DocBackup"

REM Create the destination folder if it doesn't exist
if not exist "%destination%" (
    mkdir "%destination%"
)

REM Copy all .docx files
copy "%source%\*.docx" "%destination%"

echo Backup completed successfully.
pause
```

## OUTPUT

![image](https://github.com/user-attachments/assets/f02e3d53-73a6-4bba-8021-24d8be760ad3)



# RESULT:
The commands/batch files are executed successfully.

