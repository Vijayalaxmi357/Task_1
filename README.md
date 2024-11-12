
 # VSDSquadronMini Research Internship - 20th October Cohert
 
<h2>The program is based on RISC-V architecture and uses open-source tools to teach people about VLSI and RISC-V</h2><br>

### Instructor: Kunal Ghosh
### Student Name: Vijayalaxmi</li>
### College Name:B.M.S college of engineering ,Bengaluru
<details>
 <summary>
 <h2> TASK-1 </h2> 
<h3>Installation of RISC-V toolchain using VDI. Uploading the snapshot of complied code and RISC-V Objdmp on GitHub.</h3>
 </summary>
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

### COMPILE AND EXECUTE A SIMPLE C CODE USING GCC COMPILER
    $   cd <br/>                           Navigate to home directory:<br>
    $   gedit filename.c & <br/>         This opens a blank file with filename.c, type the c code
    
![oracle VMBox](https://github.com/user-attachments/assets/ec510c91-5706-4d7f-abd5-e825ae070f5e)
![login](https://github.com/user-attachments/assets/e4a40158-1875-4eb2-adc1-0f23a57f1025)

Save the file<br> 
Come back to terminal<br>
Press entre to come to the home prompt<br>
To see the results Run the following commands

    $    gcc filename.c <br>
    $    ./a.out <br>
![open terminal](https://github.com/user-attachments/assets/0240e637-7e73-43dc-b563-30a3ee793034)
![gedit](https://github.com/user-attachments/assets/a6e3c9c5-35de-45fa-8165-34ea4e4307de)

Change the value of n in filename.c <br>
Recompile and see the results <br>
To see the code in terminal type as cat sum1ton.c<br>
![cat sum1ton](https://github.com/user-attachments/assets/615382a8-e491-41a4-affc-dbbf6eb0daa4)

To get riscv assembly code the command is<br>
![riscv](https://github.com/user-attachments/assets/a0d99dc6-5f12-4d19-92d0-357dc59c03b9)

for only required code type "less" and search for" /main"<br>
![assembly](https://github.com/user-attachments/assets/5451aea1-152f-4bed-91b2-22f2c9cfb19e)

![req assembly code](https://github.com/user-attachments/assets/ccbcd4eb-c58c-4d16-ba64-d64122d4416e)
</details>
<br>
<hr>

<details>
 <summary>
 <h2> TASK-2</h2> 
<h3>Spike simulation and observation with -O1 and -Ofast and bulding a simple application using c code using Risc-v Spike</h3>
 </summary>


## Simulation using spike application <br>
Type the command spike -d pk sum1ton.c<br>
![spike 1](https://github.com/user-attachments/assets/53dd047c-dbd9-43e3-9b07-352736fee6b7)


## Debuggig using spike we get<br> 
![spike simulation](https://github.com/user-attachments/assets/72473a0d-ee89-458e-9535-678bc376b069)

## Simple application using c code with spike simulaion
![c code](https://github.com/user-attachments/assets/360609f5-8721-404f-9bcd-89d0535cc7bf)

## Assembly code
![spike 2](https://github.com/user-attachments/assets/2812371d-dcf2-4a28-acc7-5a951dd25701)

![spike3](https://github.com/user-attachments/assets/2eff46d3-37af-4ee7-b7ef-bece33dbe1fe)<hr>
</details>
<br>
<hr>

<details>
 <summary>
 <h2> TASK-3</h2> 
<h3> 1.RISC-V instruction types</h3><br>
<h3> 2.Identifying 15 unique RISC-V instructions from riscv-objdmp of application code</h3><br>
<h3> 3.Identifying exact 32-bit instruction code in the instruction type format for 15 unique instructions</h3><br>
<h3> 4.Uploading the 32-bit pattern on Github</h3>
 </summary>

<li>
<oi>
 R Type instruction set</oi>



![image](https://github.com/user-attachments/assets/42f41b10-d5a4-472b-9e47-019becd17fe7)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RISC-V Instruction Formats</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            line-height: 1.6;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        th {
            background-color: #f2f2f2;
            text-align: left;
        }
        .code-block {
            background-color: #f4f4f4;
            padding: 10px;
            font-family: monospace;
            border-radius: 5px;
            margin: 10px 0;
        }
    </style>
</head>
<body>

<h1>RISC-V Instruction Formats</h1>
<p>RISC-V instructions have a fixed length of 32 bits and are divided into various formats, each tailored to specific types of operations. Each instruction format determines how the 32 bits are divided among operation codes, register addresses, and immediate values. Here are the primary RISC-V instruction formats:</p>

<h2>1. R-type (Register) Format</h2>
<p>Used for operations that involve only registers (e.g., arithmetic, logic operations).</p>
<div class="code-block">
    | 31-25  | 24-20 | 19-15 | 14-12 | 11-7  | 6-0    |<br>
    | funct7 | rs2   | rs1   | funct3| rd    | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rs1</strong>: First source register (5 bits)</li>
    <li><strong>rs2</strong>: Second source register (5 bits)</li>
    <li><strong>rd</strong>: Destination register (5 bits)</li>
    <li><strong>funct3</strong>: Function code for additional operation spec (3 bits)</li>
    <li><strong>funct7</strong>: Additional function spec (7 bits)</li>
</ul>
<p><strong>Example instruction:</strong> ADD rd, rs1, rs2</p>

<h2>2. I-type (Immediate) Format</h2>
<p>Used for operations that involve an immediate value (e.g., loads, arithmetic with constants).</p>
<div class="code-block">
    | 31-20      | 19-15 | 14-12 | 11-7  | 6-0    |<br>
    | imm[11:0]  | rs1   | funct3| rd    | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rs1</strong>: Source register (5 bits)</li>
    <li><strong>rd</strong>: Destination register (5 bits)</li>
    <li><strong>funct3</strong>: Function code (3 bits)</li>
    <li><strong>imm[11:0]</strong>: 12-bit immediate value</li>
</ul>
<p><strong>Example instruction:</strong> ADDI rd, rs1, imm</p>

<h2>3. S-type (Store) Format</h2>
<p>Used for store instructions, where data is stored in memory.</p>
<div class="code-block">
    | 31-25      | 24-20 | 19-15 | 14-12 | 11-7      | 6-0    |<br>
    | imm[11:5]  | rs2   | rs1   | funct3| imm[4:0]  | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rs1</strong>: Base register for memory address (5 bits)</li>
    <li><strong>rs2</strong>: Source register for data to store (5 bits)</li>
    <li><strong>funct3</strong>: Function code (3 bits)</li>
    <li><strong>imm[11:5]</strong>, <strong>imm[4:0]</strong>: Immediate value split across two fields (12 bits total)</li>
</ul>
<p><strong>Example instruction:</strong> SW rs2, offset(rs1)</p>

<h2>4. B-type (Branch) Format</h2>
<p>Used for conditional branches.</p>
<div class="code-block">
    | 31-25      | 24-20 | 19-15 | 14-12 | 11-7      | 6-0    |<br>
    | imm[12|10:5] | rs2   | rs1   | funct3| imm[4:1|11] | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rs1</strong>, <strong>rs2</strong>: Registers for comparison (5 bits each)</li>
    <li><strong>funct3</strong>: Function code (3 bits)</li>
    <li><strong>imm[12|10:5|4:1|11]</strong>: 13-bit immediate offset value for the branch</li>
</ul>
<p><strong>Example instruction:</strong> BEQ rs1, rs2, offset</p>

<h2>5. U-type (Upper Immediate) Format</h2>
<p>Used for loading 20-bit constants into the upper part of a register.</p>
<div class="code-block">
    | 31-12               | 11-7  | 6-0    |<br>
    | imm[31:12]          | rd    | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rd</strong>: Destination register (5 bits)</li>
    <li><strong>imm[31:12]</strong>: 20-bit immediate value</li>
</ul>
<p><strong>Example instruction:</strong> LUI rd, imm</p>

<h2>6. J-type (Jump) Format</h2>
<p>Used for jump and link instructions, typically for function calls.</p>
<div class="code-block">
    | 31-12               | 11-7  | 6-0    |<br>
    | imm[20|10:1|11|19:12] | rd    | opcode |
</div>
<p><strong>Fields:</strong></p>
<ul>
    <li><strong>opcode</strong>: Operation code (7 bits)</li>
    <li><strong>rd</strong>: Destination register (5 bits)</li>
    <li><strong>imm[20|10:1|11|19:12]</strong>: 21-bit immediate offset value for the jump</li>
</ul>
<p><strong>Example instruction:</strong> JAL rd, offset</p>

<h2>Summary Table</h2>
<table>
    <tr>
        <th>Format</th>
        <th>Purpose</th>
        <th>Field Breakdown</th>
    </tr>
    <tr>
        <td>R-type</td>
        <td>Register-based operations</td>
        <td>opcode, rd, funct3, rs1, rs2, funct7</td>
    </tr>
    <tr>
        <td>I-type</td>
        <td>Immediate operations & loads</td>
        <td>opcode, rd, funct3, rs1, imm[11:0]</td>
    </tr>
    <tr>
        <td>S-type</td>
        <td>Stores</td>
        <td>opcode, imm[11:5], rs2, rs1, funct3, imm[4:0]</td>
    </tr>
    <tr>
        <td>B-type</td>
        <td>Branching</td>
        <td>opcode, imm[12|10:5|4:1|11], rs2, rs1, funct3</td>
    </tr>
    <tr>
        <td>U-type</td>
        <td>Upper immediate loads</td>
        <td>opcode, rd, imm[31:12]</td>
    </tr>
    <tr>
        <td>J-type</td>
        <td>Jumps</td>
        <td>opcode, rd, imm[20|10:1|11|19:12]</td>
    </tr>
</table>

<p>These formats provide a consistent structure across instruction types, making RISC-V a simple and modular architecture suitable for a wide range of applications.</p>

</body>
</html>

</details>















