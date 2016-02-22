# payslip

### Problem  ###
pay period = per calendar month
gross income = annual salary / 12 months
income tax = based on the tax table provide below
net income = gross income - income tax
super = gross income x super rate

Note: All calculation results should be rounded to the whole dollar. If >= 50 cents round up to the next dollar increment, otherwise round down.
Tax Table

Taxable income   Tax on this income
0 - $18,200     Nil
$18,201 - $37,00019c for each $1 over $18,200
$37,001 - $80,000$3,572 plus 32.5c for each $1 over $37,000
$80,001 - $180,000$17,547 plus 37c for each $1 over $80,000
$180,001 and over$54,547 plus 45c for each $1 over $180,000

Example Data
Say for example the employee’s annual salary is $60,050 and the super rate is 9% how much will this employee be paid for the month of March?

pay period = 01/12/2016
gross income = 60,050 / 12 = 5,004.16666667 (round down) = 5,004
income tax = (3,572 + (60,050 - 37,000) x 0.325) / 12  = 921.9375 (round up) = 922
net income = 5,004 - 922 = 4,082
super = 5,004 x 9% = 450.36 (round down) = 450

Here is the csv input and output format we suggest (but feel free to use any format you want):

Input: 
first name, last name, annual salary, super rate (%), payment start date
David,Rudd,60050,9%,01/03/2016
Ryan,Chen,120000,10%,01/04/2016

Output: 
full name, pay period, gross income, income tax, net income, super
David Rudd,March,5004,922,4082,450
Ryan Chen,April,10000,2696,7304,1000


### Assumption ###
- Input File is not large enough that it can be loaded into memory
- If input csv file has format problem, the program will throw exception and exit with partial payslip generated

### Implementation ###
Using Ruby 2.2.1

### Usage ###
Usage:
    payslip [OPTIONS]

Options:
    -v, --verbose                 enable debugging
    -i, --input INPUT_CSV         Input CSV File
    -o, --output OUTOUT_CSV       Output CSV File, default payslip.csv
    -h, --help                    print help
    

