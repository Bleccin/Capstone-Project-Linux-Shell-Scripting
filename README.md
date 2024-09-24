Project https://app.darey.io/learning-path/cohortproject/641e2181fb3fa7f00650d03a/project/65cc6d111b769a6a34f92520
# Capstone-Project-Linux-Shell-Scripting
I crerated a directory named " Linux_Shell_Scripting for the project.
I created a bash script file called multiplication_table.sh
I performed the following actions on the script.
a. added shebang #!/bin/bash
b. added a prompt for the user to enter a number for the multiplication table
c. added another Prompt the user to choose between a full or partial table
d. Initialized the starting variable for the multiplication loop.
e. Use an if statement to check if the user selected a partial table.
f. Prompt the user for the starting and ending numbers (1-10) if the user had selected the partial table.
g. Used a nested if statement to Validate that the start number is less than the end and within range.
h. Used a While loop to loop through the range of the selected range of number and print out the partial multiplication table.
i. Added an elseif statement to takecare of when the range is invalid.
j. The elseif statement uses a While loop through 1 to 10 to display the full multiplication table.
k. I closed the nested loop with 'fi' after the elseif statement.
l. Added a final else statement for the main if statement to cater for when the selects a full table.
m. Used a While loop to loop through 1 to 10 and print the full multiplication table.
n. Closed the if statement with 'fi'

Testing the script
a. I tested the full table by selecting a number and f. The result was that the full multiplication table of the selected number was displayed.
b. I tested the partial table by selecting a number and p, selecting a starting and ending number. The result was that the partial multiplication table was displayed.
c. I tested Invalid range by selecting a number and p, selecting a starting number and ending number out of range. The result was that an invalid range was displayed and a full multiplication table of the selected number was displayed.
