# vendingMachine
vending machine coding challenge
instructions:
1. select config and insert pin(1234) for security purposes
2. select a json file. if it is not a json file, it will error and if the json file's format
is not corrent, it will also error.
3. after loading the config, select buy 
4. choose the corresponding code for the products
5. enter payment, numbers only. if non number is entered, it will prompt an error.
if the payment is less than the price, it will prompt an error.
6. when the payment is successful, the change will be displayed.
7. the user will have an option to buy again or close the program.
my approach:
first is imported org.json in order to read json files.
next is i created a products and config class.

upon reading the json file, the product data will be saved in an ArrayList while the
config will be saved in the config class.

in the products class, i created a function to display all the products.
i created a string that will hold the details of the products for viewing purposes.
i iterated through the array to get all the products, if the products stock is 0 then it will
not be added into the string.

i set up a row count and column count for the product codes.
i created a function to convert the row number into letters.
once the row count is greater than the stated rows in the config,
it will go into new line and reset the counting of rows and add column count

i concatenated the converted row number and column count to created product code which
i set into the current product in the array list

i then added the product code plus the product name to the string for displaying purposes

i also created a fucntion to check if the product code exists, i iterated through the array
and return its position

in the main menu, if the user choose config it will prompt a password because i think only
authorized personnel may upload a config file into thje vending machine

when the user choose the buy option

if the arrayList is empty, the program will prompt an error and return to the main menu

if its successfull, the program will call the showProducts function and will
display the products together with its product code.

the user will need to input the product code, if the user input nothing then the
program will prompt and error. also if the program does not find any match and it 
will prompt an error.

when the user input a valid product code, that products code position will be saved into
a variable.

after that is the payment. if the user input letters then the program will error, only number
is accepter for the payment. also if the product price is greater than the payment then
the program will prompt an error and ask for payment again.

if the payment is in number and is greater or equal with the product price, the program will
display the difference of the payment and product price. the selected products current amount
will also be deducted by 1.

after the transaction, the user will have the choice to buy again or close the program.
