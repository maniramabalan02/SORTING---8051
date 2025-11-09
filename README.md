
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

<img width="1919" height="257" alt="MAGESH KUMAR C 212224060143 DESCENDING ORDER IP" src="https://github.com/user-attachments/assets/16f9ce0e-4bbd-428d-8f16-58b49a5324dc" />

<BR>
<BR>
<BR>
After execution: D:0x40H:

<img width="1714" height="246" alt="Screenshot 2025-10-23 091022" src="https://github.com/user-attachments/assets/b738a317-d2b0-419b-92aa-5deb1af93a1b" />

<BR>
<BR>
<BR>


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

<img width="954" height="275" alt="Screenshot 2025-10-23 092113" src="https://github.com/user-attachments/assets/b620eb14-9c4d-4092-99c0-7e4bbc4ebcd7" />

<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:

<img width="955" height="274" alt="Screenshot 2025-10-23 092129" src="https://github.com/user-attachments/assets/56518946-e836-45ca-ba2e-379c0a8d62e3" />

<BR>
<BR>
<BR>

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

