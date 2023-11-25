# pagod na ko 420

> COBOL Verbs are used in the Procedure Division for Data Processing. A statement always start with a COBOL Verb.

<details>
<summary> Input / Output Verbs </summary>  

> these are used to get data from the user and display the output of COBOL Programs. The following 2 verbs are used for this process.

1. Accept Verb - this is used to GET DATA such as Date, Time, and Day from the OS or directly from the User. While Getting data from the OS, FROM option is included as shown in the ff. example.

ACCEPT WS-STUDENT-NAME.  
ACCEPT WS-DATE FROM SYSTEM-DATE. 

2. Display Verb - used to display the output of a COBOL Program. Example:

DISPLAY WS-STUDENT-NAME.  
DISPLAY "System date is : " WS-DATE.  

</details>

<details> 
  <summary> Initialize Verb </summary>  
  
> used to initialize a GROUP item or an ELEMENTARY item. Data names with RENAME (an alternative name for an EXISTING data item) clause cannot be initialize.  

> Numeric data items are replaced by ZEROES while Alphanumeric / alphabetic data items are replaced by SPACES.  

> REPLACING - a term that can be initialized to the given replacing value. Example:  

INITIALIZE WS-NAME, WS-ADDRESS.  
INITIALIZE WS-ID REPLACING NUMERIC DATA BY 12345.  

</details>

<details> 
  <summary> Move Verb </summary>  
  
  > used to copy data from source data to destination data. It can be used on both ELEMENTARY and GROUP data items.

> For Group Data Items, MOVE CORRESPONDING / CORR is used.  

> For moving data from a string, MOVE(x:l) is used in which x is the STARTING POSITION and l is the LENGTH. Data will be truncated if the destination item PIC clause is < the source data item PIC clause. If the data item PIC clause is more than the ource data item PIC clause, ZEROS or SPACES will be added in the extra bytes. Refer to Sample5 in the sample programs branch.
</details>

<details> 
  <summary> Legal Moves </summary>  

|               | Alphabetic          | Alphanumeric  | Numeric    |
| ------------- |:-------------------:|--------------:|------------|
| Alphabetic    | possible            | possible      |not possible|
| Alphanumeric  | possible            | possible      | possible   |
| Numeric       | not possible        | possible      | possible   |
  
</details>

<details> 
<summary> Add Verb </summary>  
  
> used to add two or more numbers and store the result in the destination operand.

Syntax:   
ADD A B TO C D  
> In syntax-1, A, B, C are added and the result is stored in C (C=A+B+C). A, B, D are added and the result is stored in D (D = A + B + D).

ADD A B C TO D GIVING E  
> In syntax-2, A, B, C, D are added and the result is stored in E (E=A+B+C+D).

ADD CORR WS-GROUP1 TO WS-GROUP2  
> In syntax-3, sub-group items within WS-GROUP1 and WS-GROUP2 are added and the result is stored in WS-GROUP2.
  
</details>

<details> 
<summary> Subtract Verb </summary>  

> used for subtarction operations.

Syntax:  
SUBTRACT A B FROM C D  
> In syntax-1, A and B are added and subtracted from C. The result is stored in C (C = C-(A+B)). A and B are added and subtracted from D. The result is stored in D (D = D-(A+B)).

SUBTRACT A B C FROM D GIVING E
> In syntax-2, A, B, C are added and subtracted from D. The result is stored in E (E = D-(A+B+C))

SUBTRACT CORR WS-GROUP1 TO WS-GROUP2  
</details>

<details> 
<summary> Multiply Verb </summary>  

> used for multiplication operations.

Syntax:  
MULTIPLY A BY B C  
> In syntax-1, A and B are multipled and the result is stored in B (B=A*B). A and C are multipled and the result is stored in C (C = A * C).

MULTIPLY A BY B GIVING E  
> In syntax-2, A and B are multipled and the result is stored in E (E=A*B).
</details>

<details> 
<summary> Divide Verb </summary>  
  
> used for division operations.
Syntax:
DIVIDE A INTO B
> In syntax-1, B is divided by A and the result is stored in B (B=B/A).

DIVIDE A BY B GIVING C REMAINDER R
> In syntax-2, A is divided by B and the result is stored in C (C=A/B) and the remainder is stored in R.
  
</details>

<details>
  <summary> Compute Statement </summary>  
  
  > used to write arithmetic expressions in COBOL. Can be a replacement for Add, Subtract, etc.

Example:
COMPUTE WS-NUMC= (WS-NUM1 * WS-NUM2) - (WS-NUMA / WS-NUMB) + WS-NUM3.
</details>
