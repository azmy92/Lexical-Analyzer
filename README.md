Lexical-Analyzer
================

A lexical analyzer generator tool


Input/Output configuration
--------------------------

 - input.txt which should contain all regular definitions and regular expressions, You should read all the assumptions provided in report_lexical.pdf well to make this file.
 - test.txt which will contain he program that you want to operate on it and.
 - symbol_table.txt which will contain the symbol table of the output which have many entire, 
   each of them has name and value.
 - out.txt which has the final output.

  You can run the program using any IDE
  -----------------------------------------------------

Sample Run:
------------------
>>For the following sample program
int sum , count , pass , mnt;
while (pass != 10)
{
pass = pass + 1 ;
}
And the following regular expressions
letter = a-z | A-Z
digit = 0 - 9
id: letter (letter|digit)*
digits = digit+
{boolean int float}
num: digit+ | digit+ . digits ( \L | E digits)
relop: \=\= | !\= | > | >\= | < | <\=
assign: =
{ if else while }
[; , \( \) { }]
addop: \+ | -
mulop: \* | /
The minimization of DFA is
In the file " minimization table output.txt"
The output file
keyword
id
punc
id
punc
id
punc
id
punc
keyword
punc
id
relop
num
punc
punc
id
assign
id
addop
num
punc
punc
The output Symbol table
token name --> keyword | token value --> boolean
token name --> keyword | token value --> int
token name --> keyword | token value --> float
token name --> keyword | token value --> if
token name --> keyword | token value --> else
token name --> keyword | token value --> while
token name --> punc | token value --> ;
token name --> punc | token value --> ,
token name --> punc | token value --> (
token name --> punc | token value --> )
token name --> punc | token value --> {
token name --> punc | token value --> }
token name --> id | token value --> sum
token name --> id | token value --> count
token name --> id | token value --> pass
token name --> id | token value --> mnt
token name --> relop | token value --> !=
token name --> num | token value --> 10
token name --> assign | token value --> =
token name --> addop | token value --> +
token name --> num | token value --> 1
For the following sample program
int sum , count , pass , mnt;
for (int i=0;i< sum;i++)
{
pass = pass + 1 ;
}
And the following regular expressions
letter = a-z | A-Z
digit = 0 - 9
id: letter (letter|digit)*
digits = digit+
{boolean int float}
num: digit+ | digit+ . digits ( \L | E digits)
relop: \=\= | !\= | > | >\= | < | <\=
assign: =
{ if else while }
[; , \( \) { }]
addop: \+ | -
mulop: \* | /
The output file
keyword
id
punc
id
punc
id
punc
id
punc
keyword
punc
keyword
id
assign
num
punc
id
relop
id
punc
id
addop
addop
punc
punc
id
assign
id
addop
num
punc
punc
The output Symbol table
token name --> keyword | token value --> boolean
token name --> keyword | token value --> int
token name --> keyword | token value --> float
token name --> keyword | token value --> if
token name --> keyword | token value --> else
token name --> keyword | token value --> while
token name --> keyword | token value --> for
token name --> punc | token value --> ;
token name --> punc | token value --> ,
token name --> punc | token value --> (
token name --> punc | token value --> )
token name --> punc | token value --> {
token name --> punc | token value --> }
token name --> id | token value --> sum
token name --> id | token value --> count
token name --> id | token value --> pass
token name --> id | token value --> mnt
token name --> id | token value --> i
token name --> assign | token value --> =
token name --> num | token value --> 0
token name --> relop | token value --> <
token name --> addop | token value --> +
token name --> num | token value --> 1
For the following sample program
for?? (int i=0;i< sum;i++)
{
pass = pass
And the following regular expressions
letter = a-z | A-Z
digit = 0 - 9
id: letter (letter|digit)*
digits = digit+
{boolean int float}
num: digit+ | digit+ . digits ( \L | E digits)
relop: \=\= | !\= | > | >\= | < | <\=
assign: =
{ if else while }
[; , \( \) { }]
addop: \+ | -
mulop: \* | /
The output file
keyword
error in : ?
error in : ?
punc
keyword
id
assign
num
punc
id
relop
id
punc
id
addop
addop
punc
punc
id
assign
The output Symbol table
token name --> keyword | token value --> boolean
token name --> keyword | token value --> int
token name --> keyword | token value --> float
token name --> keyword | token value --> if
token name --> keyword | token value --> else
token name --> keyword | token value --> while
token name --> keyword | token value --> for
token name --> punc | token value --> ;
token name --> punc | token value --> ,
token name --> punc | token value --> (
token name --> punc | token value --> )
token name --> punc | token value --> {
token name --> punc | token value --> }
token name --> id | token value --> i
token name --> assign | token value --> =
token name --> num | token value --> 0
token name --> relop | token value --> <
token name --> id | token value --> sum
token name --> addop | token value --> +
token name --> id | token value --> pass
  
  
