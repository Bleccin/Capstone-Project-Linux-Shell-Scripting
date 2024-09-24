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

Below is the final code and comments:
#!/bin/bash

# Prompt the user to enter a number for the multiplication table
read -p "Enter a number for the multiplication table:" num1

# Prompt the user to choose between a full or partial table
read -p "Do you want a full table or a partial table? (Enter 'f' for full, 'p' for partial):" tab

# Initialize the starting variable for the multiplication loop
numvar=1

# Check if the user selected a partial table
if [ "$tab" = "p" ];then
# Prompt the user for the starting and ending numbers (1-10)
read -p "Enter the starting number (between 1 and 10):" num2
read -p "Enter the ending number (between 1 and 10):" num3

# Validate that the start number is less than the end and within range
          if [ $num2 -lt $num3 ] && [ $num2 -le 10 ] && [ $num3 -le 10 ];then
# print the partial multiplication table for the selected number from the range selected
                  echo "The Partial multiplication table for ${num1} from ${num2} to ${num3}:"
# Loop through the range from num2 to num3 and print the partial multiplication table
                  while [ $num2 -le $num3 ]; do
                          echo "${num1} * ${num2} = $((num1 * num2))"
        num2=$(($num2 + 1)) # Increment num2
done


# If the range is invalid, show the full multiplication table instead
        elif [ $num2 -gt $num3 ] || [ $num2 -gt 10 ] || [ $num3 -gt 10 ] ;
        then
                 echo "Invalid range. Swhowing full table instead."
                 echo "The full multiplication table for ${num1}:"

# Loop through 1 to 10 to display the full table
                while [ $numvar -le 10 ] ;
                do
                        echo "${num1} * ${numvar} = $((num1 * numvar))"
                numvar=$(($numvar + 1)) #Increment numvar
        done
          fi

# If the user selected a full table, display it from 1 to 10
elif [ "$tab" = "f" ]; then
# Loop through 1 to 10 and print the full multiplication table
        echo "The full multiplication table for ${num1}:"
        while [ $numvar -le 10 ]; do
                echo "${num1} * ${numvar} = $((num1 * $numvar))"
                numvar=$(($numvar + 1)) #Increment numvar
        done
fi
