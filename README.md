
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:

<img width="1920" height="341" alt="Screenshot 2025-10-27 103742" src="https://github.com/user-attachments/assets/92ec95e6-9a12-49c4-91c3-f98903bff2bb" />


After execution: D:0x40H:

<img width="1911" height="344" alt="Screenshot 2025-10-27 103803" src="https://github.com/user-attachments/assets/77cc04af-b035-4427-943e-86bf7a7b9a65" />



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:

<img width="1885" height="279" alt="Screenshot 2025-10-27 103355" src="https://github.com/user-attachments/assets/fb2239a5-cf9a-4532-b740-1a76c2d59bf8" />

After execution:
D:0x40H:

<img width="1889" height="284" alt="Screenshot 2025-10-27 103421" src="https://github.com/user-attachments/assets/72fea225-57a0-446d-ab40-e03896b04668" />


**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

