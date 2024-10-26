

# RISCV_VSD_SquadronMini
## Lab exercises of RISCV workshop by Kunal Ghosh
## Instructor : Kunal Ghosh

### PRE-REQUISITE: Installing the required applications for the workshop - Virtual Box, Ubuntu on VBBOX and VDI files

## TASK-1: 
## A: Write a simple C code and compile it with gcc comipler. 
## B: Compile the same code with RISCV comipler to generate the assembly code for the same. Further Evaluate RISCV assembly code for the sample C code with two different options of comiplation.

## NECESSARY INSTALLATIONS
### Step 1: Setting up the virtual environment to work on
- Install Oracle Virtual Box, VMBox<br/>
- Launch Virtual Machine on VMBox<br/>
- Attach the VDI file to the Virtual Machine instance in VMBox<b>
-open the Virtual oracle<br>
![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 120841.png)
click on  "Show"<br>
 you will Enter to "ubuntu"<br>
 ![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 121056.png)
 -Right click and click on "open terminal"<br>

### Step 2: Type the word "gedit"-a word "gedit" is editor

### TASK 1A - COMPILE AND EXECUTE A SIMPLE C CODE USING GCC COMPILER
    $   cd <br/>                           Navigate to home directory:<br>
    $   gedit filename.c & <br/>         This opens a blank file with filename.c, type the c code
    
![image](C:\Users\vijay\Pictures\gedit.png)
Save the file<br> 
Come back to terminal<br>
Press entre to come to the home prompt<br>
To see the results Run the following commands

    $    gcc filename.c <br>
    $    ./a.out <br>
![image](C:\Users\vijay\Pictures\Task1.png)
Change the value of n in filename.c <br>
Recompile and see the results <br>
To see the code in terminal type as cat sum1ton.c<br>
![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-22 125222.png)
To get riscv assembly code the command is<br>
![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-22 233733.png)
for only required code type "less" and search for" /main"<br>
![image](C:\Users\vijay\Pictures\assembly.png)




