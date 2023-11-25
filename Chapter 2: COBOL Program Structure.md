# The Structure of a COBOL Program Consists of Divisions as shown below

Program -> Divisions -> Sections -> Paragraphs -> Sentences -> Statements -> Characters

**Sections** - a collection of paragraphs

**Paragraphs** - a subdivision of a section / division that can be either user-defined or a predefined name followed by a period and consists of zero or more sentences / entries.

**Sentences** - combination of one or more statements and appear ONLY in the **_Procedure Divsion_** and must end with a period.

**Statements** - meaniningful cobol statements that perform some processing.

**Characters** - lowest in the hierarchy and can not be divisible.

# Divisions of a COBOL Program

1. _**Identification Division**_ - the first and ONLY mandataroy division of every COBOL Program in which the compiler uses this division to identify the program.

In this division, the PROGRAM-ID specifies the program name that can only have 1-30 characters and is the only mandatory paragraph.

2. _**Environment Division**_- used to specify INPUT and OUTPUT Files of the Program. This division also describes the specific computer equipment and device that will be used by the program. This division consists of 2 sections.

**Configuration Section** - provides info about the system on which the program is written and executed. It consists of two paragraphs.

Source Computer - system used to compile the program.

Object Computer - system used to executed the program.

**Input-Output Section** - provides info about the files to be used in the program. Also consists of 2 paragraphs.

File Control - provides info of external data sets used in the program.

I-O control - provides info of files used in the program.

3. _**Data Division**_ - used to define the variables used in the program. This division consists of four sections.

File Section - used to define the record structure of the file.

Working-Storage Section - used to declared temporary variables and file structures which are used in the program.

Local-Storage Section - similar to the working-storage with its difference is that the variables will be allocated and initialized every time a program starts execution.

Linkage Section - used to describe the data names that are receivd from an external program.

4. _**Procedure Division**_ - used to include the logic of the program. This consists of executable statements using defined variables in the data division. The last statement to be executed is either STOP RUN which is used in the calling programs or EXIT PROGRAM which is used in the called programs.
