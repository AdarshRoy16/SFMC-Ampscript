# SFMC-Ampscript
%%[/* This repository will help in you getting pro with Ampscript*/]%%

AMPscript functions work in much the same way as they do in Microsoft Excel; that is, parameters are set for a predefined function, which are interpreted and, in turn, return a value. Several AMPscript functions are identical to Excel functions – while some functions are named differently, they share the same parameters and output the same result as Excel.

The example below compares the SUM Excel function with the Add AMPscript function, where two numbers are passed as arguments to the function. In this case, both functions will output the value 3.

Excel SUM function
=SUM(1,2)
Copy
AMPscript Add Function
%%=Add(1,2)=%%
Copy
There are a total of 15 comparable functions between Excel and AMPscript which accept the same parameters and output the same result, as indicated in the table below.

Excel Functions	              AMPscript functions
CHAR	                        Char
CONCATENATE	                  Concat
FIND	                        IndexOf
IF	                          IIf
ISBLANK	                      Empty
LEN	                          Length
LOWER	                        Lowercase
MOD	                          Mod
NOW	                          Now
PROPER	                      ProperCase
RANDBETWEEN	                  Random
SUBSTITUTE	                  Replace
SUM	                          Add
TRIM	                        Trim
UPPER	                        Uppercase

=====================================================VARIABLES==================================================================================================================
Variables are essentially ‘named containers’, where a user-defined name is applied to a defined entity, either a constant or function. Variable names are case-insensitive and can include characters or numbers, but not spaces or commas.
Variable names must begin with @ and include at least one other letter, number or underscore. 

#Eg.   var @firstName, @lastName, @membershipExpiryDate

NOTE: AMPscript is a loosely typed language and as a result, the interpreter does not enforce variables to be declared. However, it’s best practice to do so, to ensure the variable name is added to the Variables Dictionary.
=====================================================SETTING-VARIABLES==========================================================================================================

Once a variable is declared, it can be set. Variables are set using a syntax that comprises of four elements:

the set keyword
the variable name
a single equals symbol (=)
a personalization string, constant or AMPscript function (which can contain nested functions).
Refer to the example below, where variables are set as a personalization string (@firstName), AMPscript function (@localDate) and constant (@promotionEndDate):
#Eg.

%%[

var @firstName, @localDate, @promotionEndDate

set @firstName = FirstName
set @localDate = SystemDateToLocalDate(Now())
set @promotionEndDate = '10/15/2018'

]%%
