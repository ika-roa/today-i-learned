# Number formats in f-strings

Formatted strings in Python 3.6 and higher are prefixed with an f: `f" text {replacement_field} text ... "`. Inside the quotes the f-string consists of two kinds of parts: (1) regular string literals, i.e., **text**, and (2) **replacement fields** containing Python expressions for evaluation along with formatting control.

A replacement field is signaled by a pair of curly braces: `{ }`  and consists of a Python expression for evaluation with optional debugging mode (=), type conversion (!), and format specification (:) --> `{f-expression = !conversion:format_specifier}`


### Format specifier options

**Sign**

+: a sign is used for both positive and negative numbers
-: a sign is used only for negative numbers (default)
space: leading space for positive numbers and minus sign for negative

**Precision**

. notation indicating how many digits displayed for floats.

**Type**

- e, E: Scientific notation (with lowercase e or uppercase E)
- f, F: Fixed-point notation
- g, G: General format (fixed point or exponential depending on magnitude). With the \#-option (`#g`, `#G`): Keep any trailing zeros and the decimal point. Otherwise, remove insignificant trailing zeros and unflanked decimal point.
- %: Percentage (multiplies number by 100)

https://cheatography.com/brianallan/cheat-sheets/python-f-strings-number-formatting/


Examples: 

`import math`
`variable = math.pi * 1000*`
`f"{variable}"` --> '3141.592653589793'

`f"{variable:f}"` --> '3141.592654'
`f"{variable:.2f}"` --> '3141.59' *two decimal places*
`f"{variable:.3f}"` --> '3141.593' *three decimal places*
`f"{variable:,.2f}"` --> '3,141.59' *two decimal places and a comma*
`f"{variable:+,.2f}"` --> '+3,141.59' *as above, with forced plus sign*


`f"{variable:e}"` --> '3.141593e+00' *exponent*
`f"{variable:.2e}"` --> '3.14e+03' *two decimal places*
`f"{variable:.3e}"` --> 3.142e+03' *three decimal places*
`f"{variable:#.2e}"` --> '3.00e+03' *two decimal places and trailing zeros*
`f"{variable:.2E}"` --> '3.14E+03' *capital "E"*

`f"{variable:%}"` --> '314.159265%' *Percentage*
