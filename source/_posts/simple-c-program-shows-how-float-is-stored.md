---
title: Simple C program shows How Float is stored
date: 2022-02-19 11:12:19
tags:
  - C programming
  - Floating point
  - Computer memory
  - Data representation
cover_detail: /2022/02/19/simple-c-program-shows-how-float-is-stored/1.png
cover_index: /2022/02/19/simple-c-program-shows-how-float-is-stored/450.png
---
This is a simple code to demonstrate how a double is stored in computer memory.

To understand the concept, please read the details in the [API Floating Point Data Types](https://receiverhelp.trimble.com/oem-gnss/index.html#API_FloatingPointDataTypes.html) link.

Click [Here](https://github.com/KenRen98/How-Double-Float-is-Stored) to view the source code.

Example Output:

```bash
[root@localhost ~]# gcc ShowDoubleConversion.c -lm
[root@localhost ~]# ./a.out

Please enter a double number: 7464.1648

Double: 7464.164800
RawDouble: 40BD282A30553261

Dec Form:
*****************
Sign: 0
Exponent: 1035
Fraction: 3703336361865825

Hex Form:
*****************
Sign: 0
Exponent: 40B
Fraction: D282A30553261

Conversion:
*****************
Sign: Positive
Exponent: 12
Binary Fraction: 1101001010000010101000110000010101010011001001100001
Decimal Fraction: 1.822306
Raw Double in Decimal Calculation: 7464.164800=1x1.822306x2^12

Double Check Answer: 7464.164800
[root@localhost ~]#
