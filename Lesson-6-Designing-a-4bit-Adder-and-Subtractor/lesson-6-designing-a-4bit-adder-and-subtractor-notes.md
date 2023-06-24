# Lesson 6 - Designing a 4-bit Adder and Subtractor

## Addition

The process of addition is a fundamental arithmetic operation that forms the foundation of computer systems. In order to build a computer, it is essential to comprehend the creation of a mechanism capable of combining two numbers.

When we perform addition with decimal numbers, we typically rely on a more intricate addition table that incorporates all conceivable combinations of digits ranging from 0 to 9. However, when adding binary numbers, a much simpler table suffices, considering there are only two possible digits: 0 and 1. Memorizing and working with this binary addition table is easier due to its reduced number of entries and simpler rules for combining the digits.

|   +   |  0  |  1  |
|:-----:|:---:|:---:|
|   0   |  0  |  1  |
|   1   |  1  | 10  |

*0 plus 0 equals 0.*

*0 plus 1 equals 1.*

*1 plus 0 equals 1.*

*1 plus 1 equals 0, carry the 1.*


We add two binary numbers column by column beginning with the rightmost column:

<div style="border-bottom: solid 2px black; width: fit-content; padding-bottom: 2px">
<div style="text-indent: 13px"> 01100101</div>
<div>+  10110110</div>
</div>
<div style="margin-left: 5px; padding-top: 2px">100011011</div> 

There is a connection between logic gates and binary addition. Let's look at the table of the carry bit:
| carry |  0  |  1  |
|:-----:|:---:|:---:|
|   0   |  0  |  0  |
|   1   |  0  |  1  |

This is the identical to the output of the **AND** gate: 
| AND |  0  |  1  |
|:---:|:---:|:---:|
|  0  |  0  |  0  |
|  1  |  0  |  1  |

Next for the sum bit which turns out to be not quite straightforward as the carry bit: 
| +sum |  0  |  1  |
|:----:|:---:|:---:|
|   0  |  0  |  0  |
|   1  |  1  |  0  |

**OR** and **NAND** logic gates are close what we want to except for sum bit case. So let's connect both an **OR** gate and **NAND** to the same inputs:

<img src="assets/or_nand.png" width="200" height="100">

This circuit called the **Exclusive OR** or **XOR** gate. And finally, instead of drawing **AND** and **OR** gates we can simply draw a box which is labeled *Half Adder*. It adds two binary digits and gives a sum bit and carry bit. 

<img src="assets/half_adder.png" width="200" height="100">

The Half Adder, although useful for adding two binary numbers, does not account for the inclusion of a carry bit from a previous addition. Suppose we want to add the binary numbers 101 and 110. In this case, the addition of the rightmost column (1 + 0) can be handled by a Half Adder, resulting in a sum of 1 and no carry. However, when we move to the second column from the right, we encounter a carry from the previous column (represented as 1).

<div style="border-bottom: solid 2px black; width: fit-content; padding-bottom: 2px">
<div style="text-indent: 13px">101</div>
<div>+ 110</div>
</div>
<div style="margin-left: 5px; padding-top: 2px">1011</div> 

To handle this situation, we use two **Half Adders** and an **OR** gate.

<img src="assets/two_half_adders.png" width="400" height="100">

Here's how the process works: 
<ul>
  <li>The first Half Adder takes the two bits from the second column (0 and 1) as inputs and produces a sum of 1 and a carry of 0.</li>
  <li>The second Half Adder takes the carry from the previous column (1) and the remaining bit from the second column (0) as inputs. It produces a sum of 1 and a carry of 1.</li>
  <li>The OR gate takes the two carry outputs from the Half Adders and produces the final carry of 1.</li>
</ul>

By combining the results from the two **Half Adders** and the **OR** gate, we can accurately add three binary numbers. And instead of drawing that diagram, we can just call it *Full Adder*: 

<img src="assets/full_adder.png" width="200" height="100">

Here's a table representing the truth table for a Full Adder, which combines two Half Adders and an OR gate to accurately add three binary numbers:
|  A  |  B  | Cin | Sum | Cout |
|:---:|:---:|:---:|:---:|:----:|
|  0  |  0  |  0  |  0  |   0  |
|  0  |  0  |  1  |  1  |   0  |
|  0  |  1  |  0  |  1  |   0  |
|  0  |  1  |  1  |  0  |   1  |
|  1  |  0  |  0  |  1  |   0  |
|  1  |  0  |  1  |  0  |   1  |
|  1  |  1  |  0  |  0  |   1  |
|  1  |  1  |  1  |  1  |   1  |

In this table, the inputs A and B represent the two bits being added, while Cin represents the carry input from the previous column. The outputs Sum represent the sum bit for the current column, and Cout represents the carry output to the next column. By evaluating the inputs A, B, and Cin according to this truth table, we can determine the corresponding outputs Sum and Cout, allowing us to accurately add three binary numbers using the Full Adder.

## 4-bit Adder 

The table that we provided represents a truth table for a 1-bit adder. To present a 4-bit adder, we would need to extand the structure to include inputs and outputs for each bit position(A[3:0], B[3:0]), their corresponding sum bits (S[3:0]) and carry-out(C[3:0]).

<img src="assets/4_bit_adder.jpg" width="200" height="100">

 The 4-bit Binary Adder is illustrated in the diagram below consists of three full adders and one half adder. The input of each full adder receives the corresponding bits 'A3 A2 A1 A0' and 'B3 B2 B1 B0', representing the two binary numbers to be added. The output of the adder is denoted as 'C4 S3 S2 S1 S0', with 'C4' representing the final carry and 'S3 S2 S1 S0' representing the resulting sum. The initial component is a half-adder that takes A0 and B0 as inputs and generates a sum output S0 along with a carry bit C1. Alternatively, the first component can be a full adder, but in that case, the input carry C0 must be set to 0. The subsequent three components in the adder are full adders, as they receive three inputs each. These inputs include two primary binary bits and a carry bit from the preceding stage. 