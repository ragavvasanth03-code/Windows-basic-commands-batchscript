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
~~~
mkdir my-folder
~~~

## COMMAND AND OUTPUT
<img width="844" height="401" alt="image" src="https://github.com/user-attachments/assets/dfd40e3b-6268-435f-a0e3-85c4b1d2f952" />


Remove the directory "my-folder"
```
rmdir my-folder
```

## COMMAND AND OUTPUT
<img width="848" height="324" alt="image" src="https://github.com/user-attachments/assets/6d99ad58-cccc-4d80-bd4c-3875ce931466" />



Create the file Rose.txt
```
COPY CON Rose.txt
A clock in a office can never get stolen
Too many employees watch it all the time
^Z
1 file(s) copied
```

## COMMAND AND OUTPUT
<img width="637" height="269" alt="image" src="https://github.com/user-attachments/assets/7eefaddc-7ca8-432b-b1a3-e565a38c98b6" />



Create the file hello.txt using echo and redirection
```

echo “hello world” > hello.txt
type hello.txt
```

## COMMAND AND OUTPUT
<img width="738" height="308" alt="image" src="https://github.com/user-attachments/assets/342a538b-0a27-4ccb-9445-f0236365f4a5" />


Copy the file hello.txt into the file hello1.txt
```

copy hello.txt hello1.txt
```

## COMMAND AND OUTPUT
<img width="627" height="155" alt="image" src="https://github.com/user-attachments/assets/af3011f6-7705-44e3-bf65-2bf868fd2502" />


Remove the file hello1.txt
```

del hello1.txt
```


## COMMAND AND OUTPUT
<img width="570" height="357" alt="image" src="https://github.com/user-attachments/assets/affd91e0-de50-477e-9d30-1b4e8ac50c68" />


List out the file hello1.txt in the current directory
```
dir hello1.txt
```

## COMMAND AND OUTPUT
<img width="593" height="372" alt="image" src="https://github.com/user-attachments/assets/b89d8063-225f-4282-8faa-604bd679f1cc" />

List out all the associated file extensions 
```
assoc | more
```

## COMMAND AND OUTPUT
<img width="560" height="405" alt="image" src="https://github.com/user-attachments/assets/86bf8492-cf01-492c-b11d-e524818493bf" />



Compare the file hello.txt and rose.txt
```
fc hello.txt Rose.txt
```

## COMMAND AND OUTPUT
<img width="634" height="301" alt="image" src="https://github.com/user-attachments/assets/515758a5-72bd-43a6-9b34-c0afe3e403db" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%!
pause

Execute the batch file 1.bat
```




## OUTPUT
<img width="643" height="226" alt="image" src="https://github.com/user-attachments/assets/bb978a06-991e-4a7d-9c21-40efa02025f3" />



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
<img width="748" height="407" alt="image" src="https://github.com/user-attachments/assets/6b221ceb-5c73-478d-ab29-db7708e22d69" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT
<img width="505" height="212" alt="image" src="https://github.com/user-attachments/assets/4ee47422-9d0a-4a7c-bb2c-d493a645fcac" />





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
<img width="968" height="271" alt="image" src="https://github.com/user-attachments/assets/701c4163-73ce-4f73-8ae3-b5a168719414" />



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
<img width="668" height="519" alt="image" src="https://github.com/user-attachments/assets/42090f26-d921-480e-92f7-073be725abe1" />




# RESULT:
The commands/batch files are executed successfully.

