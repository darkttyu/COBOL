# The Structure of a COBOL Program Consists of Divisions as shown below

|Structure from Top to Bottom         |
|-------------
|Programs    |
|Divisions   |
|Sections    |
|Paragraphs  |
|Sentences   |
|Statements  |
|Characters  |

> Sections- a collection of paragraphs

> Paragraphs - a subdivision of a section / division that can be either user-defined or a predefined name followed by a period and consists of zero or more sentences / entries.

> Sentences - combination of one or more statements and appear ONLY in the **_Procedure Divsion_** and must end with a period.

> Statements - meaniningful cobol statements that perform some processing.

> Characters - lowest in the hierarchy and can not be divisible.

# Divisions of a COBOL Program

1. _**Identification Division**_ - the first and ONLY mandataroy division of every COBOL Program in which the compiler uses this division to identify the program.

In this division, the PROGRAM-ID specifies the program name that can only have 1-30 characters and is the only mandatory paragraph.

<details> 
  <summary> Syntax of Identification Division</summary>  
	
	IDENTIFICATION DIVISION.
 	PROGRAM-ID. PROGRAM_NAME.
	[AUTHOR. (COMMENT-ENTRY...)]
 	[INSTALLATION. (COMMENT)]
	[DATE-WRITTEN. (COMMENT)]
 	[DATE-COMPILED. (COMMENT)]
	[SECURITY. (COMMENT)]
 	[REMARKS. (COMMENT)]
</details>  

2. _**Environment Division**_- used to specify INPUT and OUTPUT Files of the Program. This division also describes the specific computer equipment and device that will be used by the program. This division consists of 2 sections.

<details>
  <summary> Configuration Section </summary>  
  
 > the configuration section provides info about the system on which the program is written and executed. It consists of two paragraphs.

Source Computer - system used to compile the program.

Object Computer - system used to executed the program.
</details>

<details> 
 <summary> Input-Output Section</summary>  
  
 > provides info about the files to be used in the program. Also consists of 2 paragraphs.

File Control - provides info of external data sets used in the program.

I-O control - provides info of files used in the program.
</details>

3. _**Data Division**_ - used to define the variables used in the program. This division consists of four sections.

File Section - used to define the record structure of the file.

Working-Storage Section - used to declared temporary variables and file structures which are used in the program.

Local-Storage Section - similar to the working-storage with its difference is that the variables will be allocated and initialized every time a program starts execution.

Linkage Section - used to describe the data names that are receivd from an external program.

4. _**Procedure Division**_ - used to include the logic of the program. This consists of executable statements using defined variables in the data division. The last statement to be executed is either STOP RUN which is used in the calling programs or EXIT PROGRAM which is used in the called programs.

# Hierarchical Structure of a COBOL Program

COBOL Programs are divided into major and minor parts namely Division, Sections, ad Paragraphs. 

**Divisions**

IDENTIFICATION, ENVIRONMENT, DATA, PROCEDURE

**Sections**

(Under Environment)

CONFIGURATION, INPUT-OUTPUT

(Under Data)

FILE, WORKING STORAGE

(Under Procedure)

Sections and Paragraphs that have user-defined names

**Paragraphs**

(Under Identification)

PROGRAM-ID, AUTHOR, INSTALLATION, DATE-WRITTEN, DATE-COMPILED, SECURITY, REMARKS (PROGRAM-ID is the only required bc it is the only executable part)

(Under Environment-Configuration)

SOURCE-COMPUTER, OBJECT COMPUTER, SPECIAL NAMES

(Under Environment I-O)

FILE-CONTROL

# COBOL Coding Form

COBOL is written in an 80-column format in which every character represents one column.

Columns 1-3 are for page numbers while Columns 4-6 are for line numbers.

Columns 1-6 is known as the **Sequence Area**. In the early days of COBOL when writing programs was done in paper, if the paper is misplaced, then there would be a difficulty of locating its part. It is for this reason that it opted to create a column for the line and page.

Typing page and line number today is OPTIONAL (kung di ko pa mababasa to di pa ko titigil sa paglalagay nito sa samples????) in writing COBOL programs since the days when programs were punched on cards are over..

Column 7 is known as the Indicator Area and is used for special purposes. A specific entry in this column has a special meaning. Special characters include:

Asterisk - indicates a COMMENT statement. This line provides remarks for the program and are ignored by the COBOL Compiler.

Forward Slash - makes the computer go to the top of a new page before priting a report.

Hyphen - indeicates that the line is a continuation of the preceding line.
 
Columns 8-72 are known as the program area. Column 8 which represents Area A, this is the stater of Division, Section Heading, File Description Heading, Records Heading and Procedure Heading.

Column 12 represents Area B in which this starts the Program Statement. This is also the Area in which comments are found. REMEMBER that every line of a sample program ends with a period. (lahat need tuldukan pati relasyon nyo, eme)

Columns 73 - 80 is the area in which it is prohibited to write a program statement because it will be just ignored by COBOL. These were used when programs when punched on cards (ewanq na lang ngayon try nyo), in order for the cards of different programs not to get mixed up.

