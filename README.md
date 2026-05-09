# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
<img width="248" height="41" alt="image" src="https://github.com/user-attachments/assets/403c843b-99fe-41cd-b7aa-22d4bf5bf386" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="265" height="42" alt="image" src="https://github.com/user-attachments/assets/27eff3f9-f898-4ed1-aa62-5aae2a30357f" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="251" height="41" alt="image" src="https://github.com/user-attachments/assets/0792e213-d387-4433-a2ee-b01cbbe518a3" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="306" height="42" alt="image" src="https://github.com/user-attachments/assets/48b2a89e-bdf3-4f0b-9258-2514535310d3" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="278" height="36" alt="image" src="https://github.com/user-attachments/assets/f2527b5a-083d-4c62-a169-b08a62daa4ec" />

Remove the file hello1.txt

## COMMAND AND OUTPUT
<img width="333" height="41" alt="image" src="https://github.com/user-attachments/assets/681f343c-c671-47b0-bd35-198df72b72b6" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="347" height="107" alt="image" src="https://github.com/user-attachments/assets/f7fb0c25-6d0d-45fc-bc4d-0ac0b68b2d72" />

List out all the associated file extensions 

## COMMAND AND OUTPUT
<img width="510" height="367" alt="image" src="https://github.com/user-attachments/assets/bbc6a61e-869f-42f0-9adf-5bf624c568ea" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="373" height="100" alt="image" src="https://github.com/user-attachments/assets/1606cbc2-b3de-4e76-a765-7b9f7709ff54" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
##PROGRAM
```
@echo off
set name=John
echo Hello, %name%
pause
```




## OUTPUT
<img width="352" height="41" alt="image" src="https://github.com/user-attachments/assets/2498af29-4891-4236-ae40-debf68310742" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
 for the continuation prompt (Y/N) gracefully.

##PROGRAM
```
@echo off

:START

set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is Even
) else (
    echo The number is Odd
)

set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid Input
goto START

:END
echo Thank You
pause
```

## OUTPUT
<img width="371" height="121" alt="image" src="https://github.com/user-attachments/assets/75bc7f08-15c3-489c-a64f-d0adaa9e375e" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

##PROGRAM
```
@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause
```


## OUTPUT
<img width="377" height="93" alt="image" src="https://github.com/user-attachments/assets/f1ab7674-6a78-4613-bef0-f778af76b8b0" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
##PROGRAM
```
@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause
```

## OUTPUT
<img width="366" height="40" alt="image" src="https://github.com/user-attachments/assets/5df9b8c9-3bcb-4ea6-b577-707b60dabb78" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
##PROGRAM
```
@echo off

:MENU
echo ====================
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo ====================

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid Choice
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File Created
pause
goto MENU

:EXIT
echo Goodbye
pause
exit
```

## OUTPUT
<img width="407" height="126" alt="image" src="https://github.com/user-attachments/assets/0a92a383-77c2-4da8-a1b2-58892252ba8a" />



# RESULT:
The commands/batch files are executed successfully.

