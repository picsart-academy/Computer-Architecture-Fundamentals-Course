# Lesson 6 - Designing a 4-bit Adder and Subtractor

## Addition

Addition is a fundamental arithmetic operation that serves as the building block for computer systems. To construct a computer, it is crucial to understand how to create a mechanism that can add two numbers together.

When adding decimal numbers, we typically rely on a more complex addition table that accounts for all possible combinations of digits from 0 to 9. However, when adding binary numbers, we only need a much simpler table that accounts for the two possible digits: 0 and 1. This binary addition table is easier to memorize and work with, as it has fewer entries and simpler rules for combining the digits.

| + | 0 | 1 |
| :---        |    :----:   |          ---: |
| 0 | 0 | 1 |
| 1 | 1 | 10 |

*0 plus 0 equals 0.*

*0 plus 1 equals 1.*

*1 plus 0 equals 1.*

*1 plus 1 equals 0, carry the 1.*


We add two binary numbers column by column beginning with the rightmost column:

<div style="width:fit-content; padding-bottom: 2px">
<div style="text-indent: 13px"> 01100101</div>
<div>+  10110110</div>
</div>
<div style="margin-left: 5px; padding-top: 2px">100011011</div> 






