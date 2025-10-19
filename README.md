# 8086-Assembly-Addition-of-5-numbers
8086 assembly language projects developed and debugged using DOSBox

# Aim:To write and execute Assembly Language Programs to perform addition of 5 numbers for the 8086 microprocessor.

# Software required:
* Personal Computer with MASM Software

# Algorithm:
1.Start the program

2.Initialize registers
Set accumulator to zero to store the sum.

3.Load the numbers
Access each number one by one from memory.

4.Add numbers
Add each number to the accumulator.

5.Store the result
Store the final sum in memory or display it.

6.Stop the program
End the execution using HLT or INT 21H .

# Program:
```asm
CODE SEGMENT 
ASSUME CS:CODE,DS:CODE 
ORG 1000H
MOV SI,2000H 
MOV CX,5 
MOV AL,0 
MOV AH,0 MOV BL,0 
L1: ADD AL,[SI] 
JNC L2 
INC BL 
L2: INC SI 
LOOP L1 
MOV [SI],AL 
MOV [SI+1],BL 
MOV AH,4CH 
INT 21H 
CODE ENDS 
END
```
# Manual calulation:
<img width="522" height="555" alt="image" src="https://github.com/user-attachments/assets/0f2b784a-1414-47b2-b461-6bd5898b4e79" />


## Output image from masm software:
<img width="640" height="480" alt="Screenshot (18)" src="https://github.com/user-attachments/assets/550632b2-9f23-42f8-ace5-a96df70bc83e" />

## RESULT:

Thus, the Assembly Language Programs for 8086 to perform addition of 5 numbers was successfully written and executed using MASM.




