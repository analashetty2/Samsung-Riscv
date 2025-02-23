#RISC-V INTERNSHIP PROGRAM

This project is based on the RISC-V internship program by Samsung.
***
<details>
<summary>
  Task 1- Development of C Program
</summary>

### Step 1: Fire up the Terminal
```bash
vsduser@vsduser-VirtualBox:~$
```

### Step 2: Direction to home 
```bash
cd
```

### Step 3: Open leafpad
```
leafpad sum1ton.c &
```

### Step 4: Write the code
```c
#include<stdio.h>
int main() {
int i,sum=0,n=5;
for(i=1;i<=n;i++) {
sum += i;
}
printf("Sum of numbers from 1 to %d is %d",n,sum);
return 0;
}
```

### Step 5: compile and run the code
```bash
gcc sum1ton.c
./a.out
```

### Step 6: compile the program in Assembly
```bash
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```

### Step 7: Disassemble  the sum1ton.o object file and enable easy scrolling
```bash
riscv64-unknown-elf-objdump -d sum1ton.o
riscv64-unknown-elf-objdump -d sum1ton.o | less
```

### Step 8: Search for the main section
```bash
/main
```

### Step 9: Compare the results with optimizations (-o1 and ofast)
```bash
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
</details>

<details>
<summary> Task 2- Simulation with spike</summary>
<hr> 
Test Spike by running a sample program (e.g. multiply.c) using both gcc compiler and RISC-V compiler and confirm that both the compilers generates same output

### Step 1: Compile and run the program in riscv using spike
```bash
spike pk multiply.o
```

### Step 2: Compile with the optimization level Ofast
```bash
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o multiplyl.o multiply.c
```

### Step 3: Generate an object dump
```bash
riscv64-unknown-elf-objdump -d multiply.o | less
```

### Step 4: Run the program with Spike debugger
```bash
spike -d pk multiply.o
```

</details>

<details>
<summary> Task 3 </summary>

## 15 Unique RISC-V Instructions and thier 32- Bit encodings:

## RISC-V instructions and thier Encodings

addi sp, sp, -32

Type:I-Type

32-bit encoding:11111111100000010000000100010011

li a5, 10

Type:I-Type

32-bit encoding:* 00000000101000000000011110010011

lui a0, 0x2b

Type:U-type

32-bit encoding:000000000000000000101010110111

sw a5, 8(sp)

Type:I-Type

32-bit encoding:00000000000010010011110100011

addi a0, a0, -752

Type:I-type

32-bit encoding:11001001000001010000010100010011

li a5, 20

Type:I-Type

32-bit encoding:00000001010000000000011110010011

sd ra, 24(sp)

Type:S-Type

32-bit encoding:0000000110001001100001010001

sw a5, 12(sp)

Type:S-Type

32-bit encoding:00000000100010010011110100011

jal ra, 10588 <puts>

Type:J-Type

32-bit encoding:00000010101111100100000011101111

addi a2, sp, 12

Type:I-Type

32-bit encoding:00000000110000010000011000010011

 addi a1, sp, 8
 
 Type:I-Type
 
 32-bit encoding:00000000100000010000010110010011

 jal ra, 10598 <scanf>
 
 Type:J-Type
 
 32-bit encoding:00000010101111110110000011101111

 lw a1, 12(sp)
 
 Type:I-Type
 
 32-bit encoding:00000000110000010010010110000011

 lw a0,8(sp)
 
 Type:I-Type
 
 32-bit encoding:00000000100000010010010100000011

 jal ra, 101e8 <__muldi3>
 
 Type:J-Type
 
 32-bit encoding:00000010100000000100000011101111

 </details>
 <details>
  <summary>Task 4 - Functional Simulation of RISC-V Core</summary>
  
  ### Step 1: Create a directory

  ### Step 2: Create the verilog files using touch command

  ### Step 3: locate the Files created and paste the code from <a href="https://github.com/vinayrayapati/rv32i/blob/main/?> repo</a>
  Get the Verilog netlist from <a href="https://github.com/vinayrayapati/rv32i/blob/main/iiitb_rv32i.v">RISC-V Core Verilog Netlist.</a>
  Get the testbench from<a href="https://github.com/vinayrayapati/rv32i/blob/main/iiitb_rv32i_tb.v">Testbench for RISC-V Core.

  ### Step 4: Compile the Files

  ### Step 5: Run the Files

  ### Step 6: Open the Files in GTKWave 

  ### Step 7: Add signals to GTKWave
</details>
<details>
  <summary> Task 5 - Project Overview</summary>

  ## RISC-V Based Temperature and Humidity Monitor

  A simple project using RISC-V board that detects distance through ultrasonic sensor and indicates it through led and buzzer.

### Components Required

- RISC-V Board (e.g., sipeed Longan Nano / HiFive1)
- ultrasonic sensor
- led
- buzzer
- Jumper Wires

</details>
  
 
