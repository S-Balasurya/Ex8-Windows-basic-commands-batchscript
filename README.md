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
<img width="887" height="111" alt="image" src="https://github.com/user-attachments/assets/ae52f32b-b61b-4ea8-89cd-95555ef49d33" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT
<img width="911" height="55" alt="image" src="https://github.com/user-attachments/assets/840b7fca-e5aa-4f26-85d7-9321a4c92176" />


Create the file Rose.txt

## COMMAND AND OUTPUT
<img width="767" height="107" alt="image" src="https://github.com/user-attachments/assets/f6c3eb94-b041-43a6-a82a-6dfc2e857d5a" />
<img width="827" height="258" alt="image" src="https://github.com/user-attachments/assets/fc934fce-3f3c-465d-9ee7-32329da002e2" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT
<img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/689624f7-cd4c-41cd-8302-f56ee2d704e9" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
<img width="671" height="62" alt="image" src="https://github.com/user-attachments/assets/d8f16b86-3f7f-4266-b29a-9f5d93db5e0a" />

Remove the file hello1.txt



List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
<img width="658" height="171" alt="image" src="https://github.com/user-attachments/assets/d67891bb-cc71-45e3-a1d1-81d2ae755e20" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="574" height="613" alt="image" src="https://github.com/user-attachments/assets/e5d8a66d-1818-4823-b635-621018e47480" />

Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT
<img width="614" height="218" alt="image" src="https://github.com/user-attachments/assets/691be1f7-2790-4015-b31e-6e145b387876" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause
```




## OUTPUT
<img width="506" height="80" alt="image" src="https://github.com/user-attachments/assets/df6d2ded-b8e3-47c6-9dd5-c1052c7ca682" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT

<img width="664" height="159" alt="image" src="https://github.com/user-attachments/assets/d437b186-576a-44d0-8961-beaa5ffe1eef" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT
<img width="550" height="204" alt="image" src="https://github.com/user-attachments/assets/b0a0aae9-6589-4ba9-9f2a-d69c37097cfb" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```

## OUTPUT
![WhatsApp Image 2026-03-11 at 8 49 11 AM](https://github.com/user-attachments/assets/516e48f9-909f-44d9-b9d5-50b1b1e1c92d)



Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

## OUTPUT

<img width="466" height="298" alt="image" src="https://github.com/user-attachments/assets/ac9ab885-3411-4327-afa1-626d56023800" />


# RESULT:
The commands/batch files are executed successfully.

