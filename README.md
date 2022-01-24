# File sort
Program has 3 positional parameters:
- Path to input file
- Path to output file
- One of the words (dec, hex, bin, str, vec)

Program sorts the lines of the file from the smallest to the largest according to the last parameter. Numbers are sorted by value. Since we have different representations of the same number (+3 and 3 or 0x0001 and 0x1), the original representation of the given number is written in the resulting file. Types:<br>
### dec
Lines are numbers from the range int32_t.
### hex
Lines are hexadecimal numbers with the prefix 0x from the max range uint32_t.
### bin
Lines are binary numbers (without prefix) from the max range uint32_t.
### str
Lines are string types, sorting is lexicographically (operator<).
### vec
Lines are numbers in decimal (int32_t) separated by a comma. They represents vectors of numbers. Program sorts them by length, in case of the same length by numbers.<br>
Example of line: 121,4,5,70,0,-1
