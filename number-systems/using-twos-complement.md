---
icon: book-open
---

# Using Two's Complement

Two's complement is a method for representing integers in binary form, particularly for encoding negative numbers. This system is widely used in computing because it simplifies the design of arithmetic circuits and makes operations like addition, subtraction, and multiplication more straightforward.

Two's complement is a pivotal concept in computer science, especially in the fields of computer architecture and digital electronics, as it is the main binary representation used for signed integers in most computer systems.

#### Positive Integers

Positive integers in two's complement are represented exactly the same as in regular binary notation. For example, the decimal number 5 is represented as 0101 in a 4-bit binary system.

#### Negative Integers

To represent a negative integer in two's complement;

1. Start with the Binary Representation: First, write out the binary representation of the number's absolute value. For example, to represent -5, start with 5, which is 0101 in binary.
2. Invert the Digits: Flip each bit of the number. So, 0101 (the binary for 5) becomes 1010.
3. Add One: Finally, add 1 to this inverted number. So, 1010 becomes 1011. This is the two's complement representation of -5.

#### Advantages of Two's Complement

* **Simplifies Arithmetic**: Two's complement allows for the use of the same hardware circuitry for addition, regardless of whether dealing with positive or negative numbers. For instance, adding -5 and 5 in two's complement results in 0000, which correctly represents 0.
* **Unique Representations**: There is a unique representation for each integer, eliminating ambiguities that arise in other systems like sign-magnitude or one's complement.
* **Range of Values**: In an n-bit system, two's complement can represent values from -2^(n-1) to 2^(n-1) - 1. For example, a 4-bit system can represent integers from -8 to 7.

#### Example

Representing -5 in a 4-bit two's complement system:

1. Binary of 5: 0101
2. Invert Digits: 1010
3. Add One: 1010 + 1 = 1011
4. Thus, -5 is represented as 1011.

#### Special Cases

* **Zero**: In two's complement, zero has only one representation, which is all zeros (0000 in a 4-bit system).
* **Most Negative Number**: The most negative number in two's complement (for example, -8 in a 4-bit system) does not have a positive counterpart due to the asymmetrical range.

### Decimal to Hexadecimal to Binary

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Decimal to Hexadecimal to Binary</p></figcaption></figure>

### Want to Know More?

The following is from the actual **Software Engineering Textbook (currently very few chapters released - expected full release later in 2025).**

If you are more interested in understanding how to represent integers using Two's Complement, look at the PDF below:

{% file src="../.gitbook/assets/Two's Complement.pdf" %}
