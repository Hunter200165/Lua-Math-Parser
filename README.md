# Lua-Math-Parser
Math equations parser written in pure Lua

# Usage of parser 
(Priorities of operations are decresing from up to down)
1) `(...)` - All between brackets will be evaluated recursively
2) `<Function_Name>[<Argument1>, <Argument2>; <Argument3>]` - Then any functions functions will be evaluated. Note: there is no space between `<Function_Name>` and `[`, but other whitespace characters are ignored.
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
3) Logical operators, all operators are bit-based (All is shown in decreasing order)
    - `not a` - NOT operator;
    - `!a` - NOT operator (C-style);
    - `a and b` - AND operator;
    - `a && b` - AND operator (C-style);
    - `a or b` - OR operator;
    - `a || b` - OR operator (C-style);
    - `a shl b` - Shift Left operator;
    - `a << b` - Shift Left operator (C-style);
    - `a shr b` - Shift Right operator;
    - `a >> b` - Shift Right operator (C-style);
