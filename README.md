# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200h	1204h
1201h	1205h
1202h	1206h
1203h	-                   |                          |

#### Manual Calculations

![WhatsApp Image 2025-09-08 at 13 53 57_7058f489](https://github.com/user-attachments/assets/07fd2470-ab21-4c91-9c0c-f91bb09f0345)


(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-09-08 at 13 47 55_08b14321](https://github.com/user-attachments/assets/43ffdf58-aa7f-40f2-bf34-621d9e95fbc3)


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|              1200h	1204h
1201h	1205h
1202h	1206h
1203h	-           |                          |

#### Manual Calculations

![WhatsApp Image 2025-09-08 at 13 53 58_681c7d13](https://github.com/user-attachments/assets/692d52ff-5aaf-43e3-8edd-ca2819df22a8)


(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-08 at 13 49 28_d7b9df93](https://github.com/user-attachments/assets/7358853c-ad87-487c-8337-722017abb431)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|             1200h	1204h
1201h	1205h
1202h	1206h
1203h	1207h            |                          |

#### Manual Calculations

![WhatsApp Image 2025-09-08 at 13 53 58_cb5e84b7](https://github.com/user-attachments/assets/ec55d924-bc13-4541-baa5-b3662b17745a)


(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-08 at 13 51 14_f75fe41a](https://github.com/user-attachments/assets/9b1b419a-ff2c-4a87-b959-25c0bf3472fd)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          1200h	               1204h
1201h	                           1205h
1202h                         	1206h
1203h                     |     	1207h               |

#### Manual Calculations

![WhatsApp Image 2025-09-08 at 13 57 21_f07e5d3b](https://github.com/user-attachments/assets/733c3ab3-5405-4312-8889-e2b71ab80120)


(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE


![WhatsApp Image 2025-09-08 at 13 53 05_f605d7fe](https://github.com/user-attachments/assets/82e914e1-1de7-4327-9479-d4e6fabcf8a8)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
