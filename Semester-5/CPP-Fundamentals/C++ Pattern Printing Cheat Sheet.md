# Pattern Printing Cheat Sheet

## Step 1: Always Analyze the Pattern

Before writing any code, ask yourself these 4 questions:

1. How many rows are there?
2. How many spaces in each row?
3. How many stars/numbers/characters in each row?
4. Which loop controls what?

- Golden Rule: Never start coding before answering these questions.

## Pattern Template

Almost every pattern follows this structure:

for(row = 1; row <= totalRows; row++)
{
    // Spaces

    // Stars / Numbers / Characters

    cout << endl;
}

## Nested Loop Logic 

for(row...)
{
    for(column...)
    {
        print;
    }
}
Outer Loop → Rows
Inner Loop → Columns (what gets printed)

Remember:

Outer loop decides how many lines.
Inner loop decides what appears on each line.

## Most Important Formulas
1. Increasing Pattern
   
*
**
***
****
*****

Stars: col <= row

2. Decreasing Pattern
   
*****
****
***
**
*

Stars: col <= totalRows - row + 1

Equivalent: col <= 6 - row    // if totalRows = 5

3. Right-Aligned Pattern
   
    *
   **
  ***
 ****
*****

Spaces: totalRows - row

Stars: row

4. Full Pyramid
   
    *
   ***
  *****
 *******
*********

Spaces: totalRows - row

Stars: 2 * row - 1

5. Inverted Full Pyramid

*********
 *******
  *****
   ***
    *

Spaces: row - 1
Stars: 2 * (totalRows - row) + 1

6.Diamond
    *
   ***
  *****
 *******
*********
 *******
  *****
   ***
    *
Think of it as:

Full Pyramid
+
Inverted Full Pyramid 

so, Skip the middle row in the lower half.

Lower loop: for(row = totalRows - 1; row >= 1; row--)

## Characters Instead of Stars
instead of

cout << "*";

Use:-

char ch = 'A';

cout << (char)(ch + row - 1);

Example:

A
BB
CCC
DDDD

## Numbers Instead of Stars

Instead of

cout << "*";

Print

cout << row;

Example:

1
22
333
4444

## Number of Spaces

Left-Aligned
*
**
***

Spaces:

0

(No spaces needed.)

## Right-Aligned
    *
   **
  ***

Spaces:
totalRows - row

## Inverted Full Pyramid
*********
 *******

Spaces:
row - 1

## Odd Number Formula

Whenever you see:

1
3
5
7
9

Immediately think:

2 * row - 1

This is one of the most common formulas in pattern printing.

## Reverse Odd Formula

Whenever you see:

9
7
5
3
1

Think:
2 * (totalRows - row) + 1

## Pattern Conversion Trick

Once your loops are correct, you can print almost anything.

Instead of:

cout << "*";

you can print:

cout << row;

or

cout << col;

or

cout << char('A' + row - 1);

The loop logic stays the same—only what you print changes.

## ⭐ Diamond Trick

Don't memorize a separate algorithm.

Just remember:

Diamond
=
Upper Pattern
+
Lower Pattern
-
Duplicate Middle Row

This idea works for many advanced patterns too. 

## General Strategy (Very Important)

Whenever you see a new pattern:

Step 1

Count:

Rows
Spaces
Stars
Step 2

Find the sequence.

Examples:

1 2 3 4 5

↓

row
5 4 3 2 1

↓

totalRows - row + 1
1 3 5 7

↓

2 * row - 1
7 5 3 1

↓

2 * (totalRows - row) + 1
Step 3

Write loops.

Never the other way around.

⭐ Formula Summary Table
Pattern	Spaces	Stars / Print Count
Half Pyramid	0	row
Inverted Half Pyramid	0	totalRows - row + 1
Right-Aligned Pyramid	totalRows - row	row
Full Pyramid	totalRows - row	2 * row - 1
Inverted Full Pyramid	row - 1	2 * (totalRows - row) + 1
Diamond	Combine Full + Inverted (skip middle row)	Same formulas

## ⭐ My Three Golden Rules ⭐

These are the three rules I want you to remember throughout your DSA journey:

1. Analyze first, code later.

Never rush into writing loops.

2. Patterns are formulas.

Don't memorize outputs.

Memorize the relationship between the row number and what gets printed.

3. Build from smaller pieces.

When you see a difficult pattern, ask:

"Can I build this using patterns I already know?"

That's exactly how we solved the diamond.

