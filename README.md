
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
 <h3> NECESSARY INSTALLATIONS<h3>
 <oi>
<li>Step 1: Setting up the virtual environment to work on</li><br>
<li>Install Oracle Virtual Box, VMBox</li><br>
<li> Launch Virtual Machine on VMBox</li><br>
<li>Attach the VDI file to the Virtual Machine instance in VMBox</li><br>
<li>open the Virtual oracle<li></oi><br>

![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 120841.png)<br>
click on  "Show"<br>
 you will Enter to "ubuntu"<br>

 ![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 121056.png)<br>
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
 <h2> TASK-3</h2> <br>
<h3> 1.RISC-V instruction types</h3><br>
<h3> 2.Identifying 15 unique RISC-V instructions from riscv-objdmp of application code</h3><br>
<h3> 3.Identifying exact 32-bit instruction code in the instruction type format for 15 unique instructions</h3><br>
<h3> 4.Uploading the 32-bit pattern on Github</h3>
 </summary>

<li>
<oi>
 R Type instruction set</oi>
<html lang="en">
<head>
    <title>RISC-V Instruction Formats</title>
    
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

![image](https://github.com/user-attachments/assets/42f41b10-d5a4-472b-9e47-019becd17fe7)

<p>These formats provide a consistent structure across instruction types, making RISC-V a simple and modular architecture suitable for a wide range of applications.</p>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RISC-V Instructions</title>
</head>
<body>
  <table border="1">
    <tr>
      <th>Instruction</th>
      <th>32-Bit Encoding</th>
    </tr>
    <tr>
      <td>li a0,0</td>
      <td>00000513</td>
    </tr>
    <tr>
      <td>li a1,0</td>
      <td>00000593</td>
    </tr>
    <tr>
      <td>li a2,0</td>
      <td>00000613</td>
    </tr>
    <tr>
      <td>ret</td>
      <td>00008067</td>
    </tr>
    <tr>
      <td>add a0, a1, a2</td>
      <td>00b50533</td>
    </tr>
    <tr>
      <td>sub a0, a1, a2</td>
      <td>40b50533</td>
    </tr>
    <tr>
      <td>jal ra, label</td>
      <td>0000006f</td>
    </tr>
    <tr>
      <td>beq a0, a1, label</td>
      <td>00050663</td>
    </tr>
    <tr>
      <td>bne a0, a1, label</td>
      <td>00050663</td>
    </tr>
    <tr>
      <td>lw a0, 0(sp)</td>
      <td>00020283</td>
    </tr>
    <tr>
      <td>sw a0, 0(sp)</td>
      <td>00022023</td>
    </tr>
    <tr>
      <td>slli a0, a0, 1</td>
      <td>00151513</td>
    </tr>
    <tr>
      <td>srli a0, a0, 1</td>
      <td>00155513</td>
    </tr>
    <tr>
      <td>andi a0, a0, 1</td>
      <td>00156513</td>
    </tr>
    <tr>
      <td>ori a0, a0, 1</td>
      <td>00157513</td>
    </tr>
  </table>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RISC-V Instructions with 32-Bit Encodings</title>
  <style>
    table {
      width: 100%;
      border-collapse: collapse;
    }
    table, th, td {
      border: 1px solid black;
    }
    th, td {
      padding: 8px;
      text-align: left;
    }
    th {
      background-color: #f2f2f2;
    }
  </style>
</head>
<body>
    <html>
      <h2>Exact 32-bit instruction code in the instruction type format for 15 unique instructions.And  32 bit pattern of instruction </h2><br>
      <h4>1.add a0, a1, a2</h4><br>
      <ul>
      <li>Type:R</li><br>
      <li>32-bit pattern:0000000 00010 00001 000 01000 0110011</li><br>
      <li>R-type: opcode 0110011, funct3 000, funct7 0000000</li>
      </ul><br>
      <h4>2.sub a0, a1, a2</h4><br>
      <ul>
      <li>Type:R</li><br>
      <li>32 bit pattern:0100000 00010 00001 000 01000 0110011</li><br>
      <li>R-type: opcode 0110011, funct3 000, funct7 0100000</li><br>
    </ul><br>
      <h4><b>3.jal ra, label</b></h4><br>
      <ul>
      <li><b>Type:</b>J</li><br>
      <li><b>32-bit pattern:</b>00000000000000000000 00001 1101111</li><br>
      <li><b>J-type:</b> opcode 1101111</li><br>
      </ul><br>
      <h4>4.beq a0, a1, label</h4>
      <ul>
      <li>Type:B</li>
      <li>32-bit pattern:0000000 00001 00010 000 0000010 1100011</li>
      <li>B-type: opcode 1100011, funct3 000</li>
    </ul><br>
      <h4>5.bne a0, a1, label</h4>
    <ul>
      <li>Type:B</li>
      <li>32-bit pattern:0000000 00001 00010 001 0000010 1100011</li>
      <li>B-type: opcode 1100011, funct3 001</li>
    </ul><br>
     <h4>6.lw a0, 0(sp)</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:000000000000 00010 010 00001 0000011</li>
      <li>I-type: opcode 0000011, funct3 010</li>
    </ul><br>
    <h4>7.sw a0, 0(sp)</h4>
    <ul>
      <li>Type:S</li>
      <li>32-bit pattern:0000000 00001 00010 010 0000010 0100011</li>
      <li>S-type: opcode 0100011, funct3 010</li>
    </ul><br>
    <h4>8.slli a0, a0, 1</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:0000000 00001 00001 001 00010 0010011</li>
      <li>I-type: opcode 0010011, funct3 001</li>
    </tr><br>
    <h4>9.srli a0, a0, 1</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:0000000 00001 00001 101 00010 0010011</li>
      <li>I-type: opcode 0010011, funct3 101</li>
    </ul><br>
     <h4>10.andi a0, a0, 1</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:000000000001 00001 111 00010 0010011</li>
      <li>I-type: opcode 0010011, funct3 111</li>
    </ul><br>
      <h4>11.ori a0, a0, 1</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:000000000001 00001 110 00010 0010011</li>
      <li>I-type: opcode 0010011, funct3 110</li>
    </ul><br>
    <h4>12.li a0,0</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:000000000000 00000 000 00001 0010011</li>
      <li>I-type: opcode 0010011, funct3 000</li>
    </ul><br>
    <h4>13.li a1,0</h4>
    <ul>
      <li>Type:I</li>
      <li>32-bit pattern:000000000000 00000 000 00010 0010011</li>
      <li>I-type: opcode 0010011, funct3 000</li>
    </ul><br>
     <h4>14.ret (jalr x0, ra, 0)</h4>
    <ul>
      <li>Type:I</td>
      <li>32-bit pattern:000000000000 00001 000 00000 1100111</li>
      <li>I-type: opcode 1100111, funct3 000</li>
    </ul><br>
    <h4><b>15.auipc t0, 4096</b></h4>
    <ul>
      <li><b>Type:</b>U</li>
      <li><b>32-bit pattern:</b>000000000001 00000 00000 0010111</li>
      <li><b>U-type:</b> opcode 0010111</li>
      </ul>
</body>
</html>

</details><br><hr>
<details>
 <summary>
 <h2> TASK-4</h2> 
<h3>Functional simulation and waveform using RISC-V verilog netlist and test bench  snapshots.</h3>
 </summary>Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment and Upload waveform
***NOTE:** Since the designing of RISCV Architecture and writing it's testbench is not the part of this Research Internship, so we will use the Verilog Code and Testbench of RISCV that has already been designed. The reference GitHub repository is : [iiitb_rv32i](https://github.com/vinayrayapati/rv32i/)***
Steps to perform functional simulation of RISCV
Create a new directory mkdir <task>

Create two files by using touch command as task_rv32i.v and task_rv32i_tb.v


Copy the code from the reference github repo and paste it in your verilog and testbench files.



To run and simulate the verilog code, enter the following command:

$ iverilog -o task_rv32i task_rv32i.v task_rv32i_tb.v
$ ./task_rv32i
To see the simulation waveform in GTKWave, enter the following command:

$ gtkwave task_rv32i.vcd
The GTKWave will be opened and following window will be appeared.


7.Output Waveform of various instructions that we have covered in TASK-2.


 </details><br><hr>

<details>
 <summary>
 <h2> TASK-5</h2> 
<h3>2-bit comparator</h3>
 </summary><br>
 <!DOCTYPE html>
<html lang="en">
<body>

<h1>2-Bit Comparator Project</h1>

<h2>Overview</h2>
<p>This project aims to design and implement a 2-bit comparator using the VSDSquadron Mini board. A 2-bit comparator is a digital circuit that compares two 2-bit binary numbers and indicates whether one number is greater than, less than, or equal to the other. The project involves designing the comparator logic using C programming in Visual Studio Code, setting up the hardware connections on a breadboard, and verifying the functionality through LEDs connected to the output.</p>

<h2>Project Objective</h2>
<p>The objective of this project is to:</p>
<ul>
    <li>Design a 2-bit comparator using C programming.</li>
    <li>Implement the designed comparator on the VSDSquadron Mini board.</li>
    <li>Verify the correct functionality of the comparator by using LEDs to display the comparison results.</li>
    <li>Gain hands-on experience in digital circuit design, C programming, and hardware implementation.</li>
</ul>

<h2>Key Components</h2>
<ul>
    <li><strong>VSDSquadron Mini Board</strong>: The main microcontroller board used for processing and logic implementation.</li>
    <li><strong>Breadboard and Jumper Wires</strong>: For building and testing the circuit.</li>
    <li><strong>LEDs</strong>: To display the comparison results. This project requires 3 LEDs.</li>
    <li><strong>Resistors</strong>: To limit the current to the LEDs. 220Ohm resistors are used in this project.</li>
</ul>

<h2>Pin Configuration</h2>
<table>
    <tr>
        <th>LED</th>
        <th>VSD SQUADRON BOARD</th>
    </tr>
    <tr>
        <td>LED1</td>
        <td>PIN4 (PD4)</td>
    </tr>
    <tr>
        <td>LED2</td>
        <td>PIN5 (PD5)</td>
    </tr>
    <tr>
        <td>LED3</td>
        <td>PIN6 (PD6)</td>
    </tr>
</table>

<h2>Functional Description</h2>
<p>
    <strong>A &gt; B</strong>: LED1 (Yellow color) lights up when <em>A</em> is greater than <em>B</em>.<br>
    <strong>A &lt; B</strong>: LED2 (Red color) lights up when <em>A</em> is less than <em>B</em>.<br>
    <strong>A = B</strong>: LED3 (Green color) lights up when both numbers are equal.
</p>

<h2>Truth Table of 2-Bit Comparator</h2>
<table>
    <tr>
        <th>A1</th><th>A0</th><th>B1</th><th>B0</th><th>A &gt; B</th><th>A = B</th><th>A &lt; B</th>
    </tr>
    <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>1</td><td>0</td></tr>
    <tr><td>0</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>0</td><td>0</td><td>1</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>0</td><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td><td>0</td></tr>
    <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>0</td><td>1</td><td>1</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>1</td><td>0</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>1</td><td>0</td><td>0</td><td>1</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td></tr>
    <tr><td>1</td><td>0</td><td>1</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
    <tr><td>1</td><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td></tr>
    <tr><td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0</td></tr>
</table>

<h2>Code for Implementation of 2-Bit Comparator using VSDSquadron Mini Board</h2>
<div class="code-block">
<pre>
#include &lt;ch32v00x.h&gt;
#include &lt;debug.h&gt;
#include &lt;stdio.h&gt;

#define LED1_PIN GPIO_Pin_4 //yellow LED
#define LED2_PIN GPIO_Pin_5 //red LED
#define LED3_PIN GPIO_Pin_6 //green LED
#define LED_PORT GPIOD

void GPIO_Config(void) {
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);
    GPIO_InitTypeDef GPIO_InitStructure;
    GPIO_InitStructure.GPIO_Pin = LED1_PIN | LED2_PIN | LED3_PIN;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(LED_PORT, &GPIO_InitStructure);
}

void compare_2bit(uint8_t a, uint8_t b) {
    GPIO_ResetBits(LED_PORT, LED1_PIN | LED2_PIN | LED3_PIN);

    if (a > b) {
        GPIO_SetBits(LED_PORT, LED1_PIN);
    } else if (a == b) {
        GPIO_SetBits(LED_PORT, LED2_PIN);
    } else {
        GPIO_SetBits(LED_PORT, LED3_PIN);
    }
}  

int main(void) {   
    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_2);
    SystemCoreClockUpdate();
    Delay_Init();
    GPIO_Config();

    for (uint8_t a = 0; a <= 3; a++) {
        for (uint8_t b = 0; b <= 3; b++) {
            compare_2bit(a, b);
            Delay_Ms(5000);
        }
    }
    
    return 0;
}
</pre>
</div>

<h2>Project Demonstration</h2><br>

![image](https://github.com/user-attachments/assets/3abe3671-4746-4acc-aeac-a71ad1e99ef2)<br>
</body>
</details><br><hr>
<details>
    <summary>
    <h2> TASK-6</h2> 
   <h3>Demonstration video</h3>
    </summary><br>
<p>A demonstration of the project can be carried out to observe the LED output based on different values of <em>A</em> and <em>B</em>.</p>

<img src="c:\Users\vijay\Downloads\comparator.jpeg"><br>
<h2>Conclusion</h2>
<p>This implementation demonstrates the use of the VSDSquadron Mini board to design a basic digital circuit. The 2-bit comparator effectively compares two binary numbers and outputs the comparison results through LEDs. This project reinforces the fundamental concepts of digital design. Overall, this project was a valuable learning experience.</p>
</html>
</details>
