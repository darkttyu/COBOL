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

3. Initialize Verb - used to initialize a GROUP item or an ELEMENTARY item. Data names with RENAME (an alternative name for an EXISTING data item) clause cannot be initialize.

Numeric data items are replaced by ZEROES while Alphanumeric / alphabetic data items are replaced by SPACES.  

REPLACING - a term that can be initialized to the given replacing value. Example:  

INITIALIZE WS-NAME, WS-ADDRESS.  
INITIALIZE WS-ID REPLACING NUMERIC DATA BY 12345.  


5. Move Verb - used to copy data from source data to destination data. It can be used on both ELEMENTARY and GROUP data items.

For Group Data Items, MOVE CORRESPONDING / CORR is used.  

For moving data from a string, MOVE(x:l) is used in which x is the STARTING POSITION and l is the LENGTH. Data will be truncated if the destination item PIC clause is < the source data item PIC clause. If the data item PIC clause is more than the ource data item PIC clause, ZEROS or SPACES will be added in the extra bytes. Refer to Sample5 in the sample programs branch. 

</details>
