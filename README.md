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

<img width="416" height="60" alt="image" src="https://github.com/user-attachments/assets/12c9083a-e8a1-45f2-8329-1360425d50b7" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT

<img width="446" height="55" alt="image" src="https://github.com/user-attachments/assets/67039439-06d3-4efa-bb7c-1f447cde15e4" />


Create the file Rose.txt

## COMMAND AND OUTPUT

<img width="464" height="64" alt="image" src="https://github.com/user-attachments/assets/397610c4-2455-4d2b-9565-a3345875321c" />



Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

<img width="539" height="70" alt="image" src="https://github.com/user-attachments/assets/c1f822e9-1e89-44da-b15c-a3287b870177" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

<img width="496" height="80" alt="image" src="https://github.com/user-attachments/assets/f8cb1fb5-95c4-4dc5-993a-852b6a4d3cc5" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

<img width="413" height="55" alt="image" src="https://github.com/user-attachments/assets/f765e0b7-e094-4669-9bba-f42aca19bc1c" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

<img width="404" height="107" alt="image" src="https://github.com/user-attachments/assets/f7414416-fe32-49d0-8e99-532a0b5936cb" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

<img width="356" height="414" alt="image" src="https://github.com/user-attachments/assets/bcde0bae-49dc-432c-b69b-41ce730e0072" />

<img width="403" height="423" alt="image" src="https://github.com/user-attachments/assets/bdbf6bef-b2fc-4d67-85bc-1fc01e01d7de" />

<img width="301" height="421" alt="image" src="https://github.com/user-attachments/assets/e9152406-e590-4fd9-910c-dd5c92748119" />

<img width="255" height="418" alt="image" src="https://github.com/user-attachments/assets/3c7d6696-261b-4eac-883a-f30b58b8528b" />

<img width="393" height="408" alt="image" src="https://github.com/user-attachments/assets/7c929d6f-5806-43da-a2ec-b463923b7fbe" />

<img width="370" height="420" alt="image" src="https://github.com/user-attachments/assets/1c4ccf72-525f-4706-b15b-7859c0b22ce0" />

<img width="304" height="407" alt="image" src="https://github.com/user-attachments/assets/59c80ced-e59c-43cc-8200-a6122ed543d0" />

<img width="390" height="418" alt="image" src="https://github.com/user-attachments/assets/1ed3ce5b-c1ea-4f96-952f-295187b92f9c" />

<img width="447" height="418" alt="image" src="https://github.com/user-attachments/assets/eff8deb0-8bab-4ec2-b5ca-e3e26a3a9be9" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

<img width="474" height="99" alt="image" src="https://github.com/user-attachments/assets/5bbb72ae-48f2-487d-935a-cbd57b47fdfa" />


## Exercise 2: Advanced Batch Scripting
1.Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

## BATCH PROGRAM
```
@echo off
set name=John
echo Hello, %name%
pause
```

## OUTPUT
<img width="429" height="60" alt="image" src="https://github.com/user-attachments/assets/83675b5a-6a91-49ec-bd52-c3d0824ac51c" />



2.Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

## BATCH PROGRAM
```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```



## OUTPUT
<img width="389" height="179" alt="image" src="https://github.com/user-attachments/assets/f428ec76-d374-43db-8aef-c92c991a156c" />





3.Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

## BATCH PROGRAM
```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```

## OUTPUT

<img width="457" height="116" alt="image" src="https://github.com/user-attachments/assets/cfde5833-e9d4-4713-8c59-987bb9ed73f1" />




4.Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## BATCH PROGRAM 
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

<img width="416" height="49" alt="image" src="https://github.com/user-attachments/assets/e809f988-c28c-4feb-aed8-9425b1b93c78" />


5.Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

## BATCH PROGRAM
```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```


## OUTPUT
<img width="241" height="97" alt="image" src="https://github.com/user-attachments/assets/25f67860-33f0-4f97-94a8-13f010953a22" />


<img width="244" height="97" alt="image" src="https://github.com/user-attachments/assets/c4535a97-12ad-450f-ae73-91f3a7b0ed51" />


<img width="255" height="100" alt="image" src="https://github.com/user-attachments/assets/c44868ee-a41c-4e6b-9d22-78cf43b97b60" />



# RESULT:
The commands/batch files are executed successfully.

