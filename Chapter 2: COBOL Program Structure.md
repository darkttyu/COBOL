# The Structure of a COBOL Program Consists of Divisions as shown below

Program -> Divisions -> Sections -> Paragraphs -> Sentences -> Statements -> Characters

**Sections** - a collection of paragraphs

**Paragraphs** - a subdivision of a section / division that can be either user-defined or a predefined name followed by a period and consists of zero or more sentences / entries.

**Sentences** - combination of one or more statements and appear ONLY in the **_Procedure Divsion_** and must end with a period.

**Statements** - meaniningful cobol statements that perform some processing.

**Characters** - lowest in the hierarchy and can not be divisible.

# Divisions of a COBOL Program

1. Identification Division - the first and ONLY mandataroy division of every COBOL Program in which the compiler uses this division to identify the program.

In this division, the PROGRAM-ID specifies the program name that can only have 1-30 characters and is the only mandatory paragraph.

2. Environment Division - used to specify INPUT and OUTPUT Files of the Program. This division also describes the specific computer equipment and device that will be used by the program.
