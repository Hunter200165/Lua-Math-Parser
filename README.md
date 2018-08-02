# Lua-Math-Parser
Math equations parser written in pure Lua

# Usage of parser 
(Priorities of operations are decresing from up to down)
1) `(...)` - All between brackets will be evaluated recursively
2) `<Function_Name>[<Argument1>, <Argument2>; <Argument3>]` - Then any functions will be evaluated. Note: there is no space between `<Function_Name>` and `[`, but other whitespace characters are ignored.
    - `pow[ a, b ]` - Raises `a` to the exponent of `b`;
    - `sqrt[ a ]` - Calculates square root out of `a`;
    - `abs[ a ]` - Returns non-negative representation of `a`;
    - `sin[ a ]` - Returns sine of `a`;
    - `cos[ a ]` - Returns cosine of `a`;
    - `tan[ a ]` - Returns tangent of `a`;
    - `log[ a ]` - Returns natural logarithm of `a`;
    - `log10[ a ]` - Returns ten-based logarithm of `a`;
    - `pi[]` - Returns pi number;
    - `floor[ a ]` - Returns floor-rounded representation of `a`;
    - `ceil[ a ]` - Returns ceil-rounded representation of `a`;
    - `rad[ a ]` - Returns converted to radians `a`;
    - `deg[ a ]` - Returns converted to degrees `a`;
    - `bits[ a, b ]` - Casts `a` to `b` amount of bits;
    - `bit[ a ]` - Casts `a` to one bit;
    - `byte[ a ]` - Casts `a` to one byte;
    - `word[ a ]` - Casts `a` to two bytes;
    - `int[ a ]` - Casts `a` to four bytes;
3) Logical operators, all operators are bit-based (All is shown in priority decreasing order)
    - `not a` - NOT operator;
    - `!a` - NOT operator (C-style);
    - `a and b` - AND operator;
    - `a && b` - AND operator (C-style);
    - `a or b` - OR operator;
    - `a || b` - OR operator (C-style);
    - `a xor b` - XOR operator;
    - `a ^ b` - XOR operator (C-style);
    - `a shl b` - Shift Left operator;
    - `a << b` - Shift Left operator (C-style);
    - `a shr b` - Shift Right operator;
    - `a >> b` - Shift Right operator (C-style);
4) `a ** b` -  Exponential operator: Raises `a` to the exponent of `b`. Same as `pow[ a, b ]`;
5) Integer division operators:
    - `a div b` - DIV operator;
    - `a // b` - DIV operator (C-style);
6) Modulus operators:
    - `a mod b` - MOD operator;
    - `a % b` - MOD operator (C-style);
7) Arithmetic operators:
    - `a * b` - Multiplication operator
    - `a / b` - Division operator
    - `a + b` - Sum operator
    - `a - b` - Subtraction operator
8) Equality operators (return 1 if equal, 0 otherwise):
    - `a = b` - Equality operator;
    - `a == b` - Equality operator (C-style);
    
#Usage example
- `floor[ sqrt[ pow[ 2, log[ 154 ] ] ] ]` - Useless math
- `sqrt[ 3**2 + 4**2 ]` - Pythagoras rule
- `(238 && 156) == (238 and 156)` - Test logic
- `((238 && 156) == (238 and 156)) << (2 xor 1) = ((154 || 12) == (154 or 12)) shl (1 ^ 2)` - Advanced logic test
- `((23 ** 2 div 2) == (23 ** 2 // 2)) && (((15 mod 2 << 1) >> 2) == ((15 % 2 shl 1) shr 2))` - Logic and arithmetics
