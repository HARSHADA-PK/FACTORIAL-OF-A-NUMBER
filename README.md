# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
OUTPUT

<img width="278" height="391" alt="Screenshot 2025-09-23 213925" src="https://github.com/user-attachments/assets/0e2ff94d-44f6-449c-af5c-45ded0c0973f" />

<img width="566" height="400" alt="image" src="https://github.com/user-attachments/assets/e363190b-359d-4ad7-9b02-fd1d149a8899" />



---
MANUAL CALCULATIONS

---
![fact](https://github.com/user-attachments/assets/9106cfba-b88b-4273-be70-a1c69661bf89)


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


