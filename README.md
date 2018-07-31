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
