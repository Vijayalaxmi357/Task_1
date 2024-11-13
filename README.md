
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
![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 120841.png)
click on  "Show"<br>
 you will Enter to "ubuntu"<br>
 ![image](C:\Users\vijay\Pictures\Screenshots\Screenshot 2024-10-26 121056.png)
 -Right click and click on "open terminal"<br>
 </details>
<details>
 <summary>
 <h2> TASK-2 </h2> 
<h3>Write a simple C code and compile it with gcc comipler. And Compile the same code with RISCV comipler to generate the assembly code for the same. Further Evaluate RISCV assembly code for the sample C code with two different options of comiplation.</h3>
 </summary>



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
 <h2> TASK-3</h2> 
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
 <h2> TASK-4</h2> <br>
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
 </summary>
 </details><br><hr>

<details>
 <summary>
 <h2> TASK-5</h2> 
<h3>Object detector using ultrasonic sensor</h3>
 </summary>
 <h4>Overview</h4><br>
The Object Detector project integrates an ultrasonic sensor with the CH32V003 RISC-V processor to detect nearby objects. By utilizing the ultrasonic sensor, the system can detect objects within its range and alert the user by switching on an LED. This project is designed for various applications, including obstacle detection, proximity sensing, and as a component in larger automated systems.

<h4>Components Required</h4><br>
<h5>1. Hardware</h5>
<ul>
<li>CH32V003 RISC-V processor</li>
<li>Ultrasonic sensor (HC-SR04)</li>
<li>LED</li>
<li>Power Supply</li>
<li>Breadboard</li>
<li>Jumper Wires</li>
</ul><br>
<h5>2. Software</h5><br>
<ul>
<li>VSCode</li>
<li>PlatformIO</li>
</ul><br>
<h4>Hardware Connections</h4><br>
<h4>The ultrasonic sensor is connected to the VSDSquadron Mini as follows:</h4><br>
<oi>
<li>TRIG PIN to PD2 on VSDSquadron Mini</li>
<li>ECHO PIN to PD4 on VSDSquadron Mini</li>
<li>GND to GND on VSDSquadron Mini</li>
<li>VCC to 3.3V on VSDSquadron Mini</li>
</oi><br>
<h4>How to Program</h4><br>

-Install PlatformIO Core : Ensure PlatformIO Core is installed on your system. Follow the installation guide provided by PlatformIO.
-Build and Upload Commands :
-Build the project: $ pio run
-Upload the firmware: $ pio run –target upload
-Clean build files: $ pio run –target clean<br>
<h4>API Reference</h4>
-USART_Printf_Init() : Initializes the USART peripheral for debugging and output.
-Delay_Ms() : Generates a millisecond delay, useful for timing and sensor control.
-GPIO_ReadInputDataBit() : Reads the state of an input pin.
-GPIO_WriteBit() : Sets or clears a specific output pin, used for controlling the LED and the ultrasonic sensor’s trigger.
-Code Snippet
#include <ch32v00x.h>

#include <debug.h>

void GPIO_Config(void) {

GPIO_InitTypeDef GPIO_InitStructure = {0};

RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);

// Configure echo and trigger pins

GPIO_InitStructure.GPIO_Pin = GPIO_Pin_0 | GPIO_Pin_4;

GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU;

GPIO_Init(GPIOD, &GPIO_InitStructure);

// Configure trigger and LED pins

GPIO_InitStructure.GPIO_Pin = GPIO_Pin_2 | GPIO_Pin_3;

GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;

GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;

GPIO_Init(GPIOD, &GPIO_InitStructure);

}

int main(void) {

uint8_t echo_status = 0;

NVIC_PriorityGroupConfig(NVIC_PriorityGroup_2);

SystemCoreClockUpdate();

Delay_Init();

GPIO_Config();

while(1) {

// Trigger ultrasonic sensor

GPIO_WriteBit(GPIOD, GPIO_Pin_2, SET);

Delay_Ms(10); // Trigger pulse width

GPIO_WriteBit(GPIOD, GPIO_Pin_2, RESET);

echo_status = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_4);

if (echo_status == 1) {

// Object detected, blink LED

GPIO_WriteBit(GPIOD, GPIO_Pin_3, SET);

Delay_Ms(2000); // LED on duration

GPIO_WriteBit(GPIOD, GPIO_Pin_3, RESET);

Delay_Ms(2000); // LED off duration

}

}

}
Working Principle
The system operates by sending a short ultrasonic pulse (triggered by PD2) and listening for an echo (received on PD4). The presence of an object within the sensor’s range reflects the pulse back to the sensor, detected as a high signal on the ECHO pin. Upon detection, the processor activates an LED to alert the user of the detected object.

Applications
Object Detection : Useful in parking assistance systems, robot obstacle avoidance, and proximity detection for home automation.
Security Systems : Employing ultrasonic sensors for motion detection in restricted areas.
Distance Measurement : Accurate distance measurements for assembly line spacing, liquid level monitoring, and height measurement of objects.
Liquid Level Detection : Using ultrasonic sensors to monitor the liquid level inside tanks, preventing unstable readings caused by wavy surfaces or bubbles.
 </details>








