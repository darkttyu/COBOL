# Sana gumana, if hinde edi kasalanan nyo : P emi


Step 1: Open Windows Powershell as Administrator and run this Command.  

	dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all
	
 	after entering the command, restart the device  

Link for Ubuntu: https://apps.microsoft.com/detail/9PDXGNCFSCZV?hl=en-US&gl=US / https://ubuntu.com/download/desktop
Link for Debian: https://apps.microsoft.com/detail/9MSVKQC78PK6?hl=en-us&gl=US / https://www.debian.org/distrib/  

If hindi sya mainstall, nasa link na rin yung guide how ifix.

Step 2: Open a Terminal / Command Prompt to Install WSL. Enter the command below. 

	wsl --install -d Ubuntu/Debian

After nito, iaask ka na mag-enter ng username and password. If walang lumalabas sayo na ***** when typing the initial password, wag ka mag-alala kasi encrypted yon hehe.  

Step 3: If hindi nyo pa naiinstall VSC. Install nyo na here. 

	https://code.visualstudio.com/download

Step 4: Install GNUCobol, eto yung compiler hehehe. You can download it using the terminal or sa website mismo.

	# update muna yung system 
	sudo apt update 

 	# dl na compiler for COBOL
 	sudo apt install gnucobol4

 	# if ayaw nyo dl nyo na lang dito
	https://gnucobol.sourceforge.io/

 Step 5: Open the Ubuntu / Debian Terminal depends sa ininstall nyo and type 

 	code

 This will open up your VSCode with WSL. If walang nagbukas sainyo edi hala

 Step 6: Install COBOL Extension and you can make your COBOL Program na yey. Eto sample program
```cobol
		IDENTIFICATION DIVISION.
		PROGRAM-ID. Sample.
		      
		DATA DIVISION.
		WORKING-STORAGE SECTION.
		01 STATEMENT PIC X(9) VALUE "AYOKO NA!".
		      
		PROCEDURE DIVISION.
			DISPLAY STATEMENT.
			DISPLAY "Ang di mag-thank you mamalasin".
			STOP RUN.
		END PROGRAM Sample.
```
 Step 7: In running your program. You must need to do the ff commands in the terminal.

	# -x means you want your program to be compiled as an executable file
 	# -o means eto yung file name nung output file nyo
	# main.cob yung file name nung program nyo
	
 	cobc -x -o output main.cob

	# After compiling, para marun nyo enter nyo to.

	./output

 	# Initially pede nyo na pagsabayin by separating them with the && operator.
	cobc -x -o output main.cob ./output

	yey marunong na sila magcobol !! 
