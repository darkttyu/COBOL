awahaha idk if need ko pa to isama here kasi i think pede namang iskim na lang to

# Character Set

The COBOL Character Set Includes _78 Characters_

A-Z Alphabet in Upper Case

a-z Alphabet in Lower Case

0-9 Numeric

Space

Plus & Minus Sign / Hyphen (+, -)
 
Asterisk (*)

/ Forward Slash

$ Currency Sign

, Comma

; : Semicolon, and Colon

. DecPoint / Period

" Quotation Marks

() Left and Right Parenthesis

<=> Greater / Less than Sign & Equal Sign

**Coding Sheet (shet tlg)**

There are 80 character positions on each line of a coding sheet and are grouped into
5 fields.

Positions 1-6 (Column Numbers) - Reserved for Line Numbers.

Position 7 (Indicator) - can have an Asterisk(comment), Hyphen(continuation), and Forward Slash (form feed).

Position 8-11 (Area A) - ALL COBOL division, sections, paragraphs, and some special entries
must begin at Area A.

Position 12-72 (Area B) - ALL COBOL statements must begin in Area B.

Position 73-80 (Identification Area) - can be used as needed by the programmer (AKALA KO PROHIBITED AREA TO????? PERO SIGE)

<details> 
<summary> Character Strings </summary>

**Character Strings** are formed by Combining Individual Characters. It can be a Comment, Literal, or COBOL word.

They must end with separators. Frequently used separators are Space, Comma, Period, Apostrophe, Left/Right Parenthesis, and Quotation Mark.

**Comment** - a character string that does not affect the execution of a program. Can be a comment line (can be written in any column) or comment entry (included in the optional paragraphs of an identification division)

**Literal** - a constant that is directly hard-coded in a program. Example is "Hello World". 2 Types of Literals are _Alphanumeric_ (literals that are enclosed in a pair of apostrophe / quotation marks) and _Numeric_ (combination of digits from 0 - 9, +, -, and decpoint in which the sign cannot be in the rightmost character and decpoint should NOT appear at the end.)

**COBOL Word** - a character string that can be a RESERVED word or a USER-DEFINED word that has a length of up to 30 Characters.

User-Defined - these are words that are used for naming files, data, records, paragraph names, and sections. You cannot use COBOL reserved words while you can use alphabets, digits, and hyphens when making user-defined words.

Reserved Words - words that are predefined in COBOL. There are 3 diff types of reserved words. 

Keywords - ADD, ACCEPT, MOVE, etc.

Special Characters - +, -, *, <, <=, etc

Figurative Constants - constant values like ZERO, SPACES, etc.

<details>
 <summary> Figurative Constants & Description </summary>

 1. HIGH-VALUES - one or more charac which will be at the highest position in DESCENDING Order.
 2. LOW-VALUES - one or more charac have zeros in binary representation.
 3. ZERO/ZEROES - one or more zero depending on the size of the variable.
 4. SPACES - one or more spaces.
 5. QUOTES - single or double quotes. (' ', " ")
 6. ALL literal - fills the data-item with Literal.
    
</details>
</details>
