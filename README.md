# first-and-follow-of-a-grammar
this code finds FIRST and FOLLOW of any given context-free-grammar

input rules:
1. first it take an integer for number of lines of production
2. it takes n lines of string as an input
3. the string should have first letter in uppercase
4. next 2 letter of string are ->
5. rest of the string can have any character
6. if you have many productions for a single non-terminal then represent it in a single line seperated by |
7. here @ is null

example:
input:
5
E->TX
X->+TX|@
T->FY
Y->*FY|@
F->(E)|@

output:
FIRST(X) :  + @
FIRST(E) :  ( * + @
FIRST(Y) :  * @
FIRST(T) :  ( * @
FIRST(F) :  ( @

FOLLOW(Y) :  $ ) +
FOLLOW(F) :  $ ) * +
FOLLOW(T) :  $ ) +
FOLLOW(E) :  $ )
FOLLOW(X) :  $ )
