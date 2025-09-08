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
|          1200h	                  1204h
           1201h	                  1205h
           1202h	                  1206h
           1203h	                   -                                         
           
#### Manual Calculations
![WhatsApp Image 2025-09-08 at 13 53 57_dbc2112c](https://github.com/user-attachments/assets/79151072-ef05-4ead-bece-7c222d130174)

(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 13 47 55_444b66a9](https://github.com/user-attachments/assets/4ad3e062-62ac-4d72-90d9-6f66266648c0)


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
|            1200h    	           1204h
             1201h	              1205h
            1202h	                 1206h
             1203h                  -                                

#### Manual Calculations
![WhatsApp Image 2025-09-08 at 13 53 58_f5da4a28](https://github.com/user-attachments/assets/2dde264b-fedf-4113-b4f8-b7956dd59fa8)


(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 13 49 28_af461a4b](https://github.com/user-attachments/assets/426cc2b8-8ef7-43fe-a928-d49c81d5f229)

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
|              
1200h	                                 1204h
1201h	                                 1205h
1202h                                	1206h
1203h	                                 1207h           


#### Manual Calculations
![WhatsApp Image 2025-09-08 at 13 53 58_e856c6fe](https://github.com/user-attachments/assets/5f6bdc16-3e04-4a5e-bc2c-9160eb8c9b76)



---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 13 51 14_a22e8397](https://github.com/user-attachments/assets/4e32b553-4c33-42e4-8dc9-f9f780686f18)


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
|        1200h                 	1204h
         1201h                 	1205h
         1202h	                  1206h
         1203h                	1207h                                           

#### Manual Calculations
![WhatsApp Image 2025-09-08 at 13 57 21_0998f052](https://github.com/user-attachments/assets/ce68e60a-d58d-43bc-bbea-193110b38a83)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-08 at 13 53 05_c6e53c3b](https://github.com/user-attachments/assets/cfe814db-d761-447d-9141-f51796b85d2f)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
