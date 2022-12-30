**Lexical-Analyzer-and-Syntax-Tree-in-Compiler-**


Implementation of lexical analyzer:

•	Tokenization of expression (expression can be i.e a+(b*c)or 3+ (5*2)digits, alphabets, characters)

•	Building regex for the expression •Output tags/ tokens of the expression (i.e.  ['a', '+', '(', 'b', '*', 'c', ')'])


Lexical analyzer is the first phase of compiler construction. It acts as a machine for given expressions and divide it into units called tokens. This process is called tokenization. Lexical analyzer then identifies each token as integer, identifier, alphabet, or operator. 
We use the re (regular expression) library in python to implement Lexical analyzer.

Steps of implementation are:
1.	Import the re library.
2.	Enter the source code on which lexical analyzation will happen.
3.	The split function divides the words into units or tokens.
4.	After that, we will check each unit one by one. 
5.	If it is a Datatype the output will be in such a format ['DATATYPE' , int].
6.	Likewise, it will check for each token and display every token with its respective type.

The output of the expression “int sum = 100 + b + c” when we pass it through lexical analyzer is:

[['DATATYPE', 'int'], ['IDENTIFIER', 'sum'], ['OPERATOR', '='], ['INTEGER', '100'], ['OPERATOR', '+'], ['IDENTIFIER', 'b'], ['OPERATOR', '+'], ['IDENTIFIER', 'c']]


Implementation of syntax tree using AST library of python:

Syntax tree is in which each leaf node describes an operand & each interior node describes an operator. The syntax tree is shortened form of the Parse Tree.

•	We use the AST (Abstract Syntax Tree) library in python to display the syntax tree of an expression. 

•	“Ast.parse” will form a syntax tree.

•	We use “dump” function to store the data in file and then display it on the output screen.

The syntax tree of expression “result = b + c” is:

Module(body=[Assign(targets=[Name(id='result', ctx=Store())], value=BinOp(left=Name(id='b', ctx=Load()), op=Add(), right=Name(id='c', ctx=Load())), type_comment=None)], type_ignores=[])
