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
![image](https://github.com/user-attachments/assets/c3eca31f-67a5-4675-ae5f-6f44cb819b79)

## COMMAND AND OUTPUT

Change to the "MyLab" directory and create an empty text file named "MyFile.txt" inside it.
```
C:\Users\admin\Mylab>echo > MyFile.txt
```
![image](https://github.com/user-attachments/assets/d37638f4-4376-4052-bd76-0715b71bfc7a)

## COMMAND AND OUTPUT

List the contents of the "MyLab" directory.
```C:\Users\admin\Mylab>dir
```
![image](https://github.com/user-attachments/assets/344db421-a605-474b-b8a9-ecaebd4e5fa9)

## COMMAND AND OUTPUT

Copy "MyFile.txt" to a new folder named "Backup" on the desktop.
```
copy "Mylab\MyFile.txt" "Backup\copy.txt"
```
![image](https://github.com/user-attachments/assets/7363479a-8dfe-4c22-a159-cb4b796f88c2)

## COMMAND AND OUTPUT

Move the "MyLab" directory to the "Documents" folder.
```
move "Mylab\*.*" "Backup"
```
![image](https://github.com/user-attachments/assets/6d269356-3db0-4a96-88eb-1815744a7d32)


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

![image](https://github.com/user-attachments/assets/b124a699-b5a9-4f82-8914-77381c943062)




# RESULT:
The commands/batch files are executed successfully.

