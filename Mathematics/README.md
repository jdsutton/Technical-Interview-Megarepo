# Mathematics

## Radix
* [Radix](https://en.wikipedia.org/wiki/Radix)
  * "In mathematical numeral systems, the radix or base is the number of unique digits, including zero, used to represent numbers in a positional numeral system. For example, for the decimal system (the most common system in use today) the radix is ten, because it uses the ten digits from 0 through 9."
* [Base Conversion](https://en.wikipedia.org/wiki/Positional_notation#Base_conversion)
* [Converting to/from Decimal](http://www.cs.trincoll.edu/~ram/cpsc110/inclass/conversions.html)

## Binary
* [Sign-magnitude](https://en.wikipedia.org/wiki/Signed_number_representations)
  * " In this approach, the problem of representing a number's sign can be to allocate one sign bit to represent the sign: setting that bit (often the most significant bit) to 0 is for a positive number or positive zero, and setting it to 1 is for a negative number or negative zero. The remaining bits in the number indicate the magnitude (or absolute value)."
* [One's complement](https://en.wikipedia.org/wiki/Ones%27_complement)
  * "The ones' complement of a binary number is defined as the value obtained by inverting all the bits in the binary representation of the number (swapping 0s for 1s and vice versa). The ones' complement of the number then behaves like the negative of the original number in some arithmetic operations"
  * "However, unlike two's complement, these numbers have not seen widespread use because of issues such as the offset of −1, that negating zero results in a distinct negative zero bit pattern, less simplicity with arithmetic borrowing, etc"
* [Two's complement](https://en.wikipedia.org/wiki/Two%27s_complement)
  * "Two's complement is a mathematical operation on binary numbers, as well as a binary signed number representation based on this operation. Its wide use in computing makes it the most important example of a radix complement. The two's complement of an N-bit number is defined as the complement with respect to 2<sup>N</sup>; in other words, it is the result of subtracting the number from 2<sup>N</sup>"

## Discrete Mathematics
* [Knuth, Concrete Mathematics - A Foundation for Computer Science](http://www.amazon.com/Concrete-Mathematics-Foundation-Computer-Science/dp/0201558025)
* [MIT - Mathematics for Computer Science](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-042j-mathematics-for-computer-science-fall-2010/)
* [University of Victoria - Discrete Math](http://www.math.uvic.ca/faculty/gmacgill/guide/index.html)

## Summation Formulas
* Σ(i=1...n, i) = n(n + 1)/n
* In general the sum of i<sup>k</sup> from 1...n is O(n<sup>k + 1</sup>)

## Recurrence Relations
* [Duke University - Recurrence Relations](https://users.cs.duke.edu/~reif/courses/alglectures/skiena.lectures/lecture3.pdf)
* [Carnegie Mellon University - Solving Recurrence Relations](http://www.cs.cmu.edu/~rweba/algf09/solverecurrencesSF.pdf)

## Probability
* [Khan Academy - Probability and Statistics](https://www.khanacademy.org/math/probability?t=table-of-contents)
* [Udacity - Intro to Statistics](https://www.udacity.com/course/intro-to-statistics--st101)

## Combinatorics
* [Khan Academy - Combinatorics](https://www.khanacademy.org/math/probability/probability-and-combinatorics-topic)
* [Wikipedia - Binomial Coefficient](https://en.wikipedia.org/wiki/Binomial_coefficient)
* [Wikipedia - Combination](https://en.wikipedia.org/wiki/Combination)
* <sup>n</sup>C<sub>r</sub>
  * ![n choose k](https://upload.wikimedia.org/math/3/8/2/382c5908d125a08662b2fedc22f4d02c.png)
  * # of combinations of r elements from a set of n
  * = n! / r! (n - r)!
* [Wikipedia - Permutation](https://en.wikipedia.org/wiki/Permutation)
* <sup>n</sup>P<sub>r</sub>
  * # of permuations of r elements from a set of n
  * = n! / (n - r)!
* Subsets
  * # of all possible subsets from a set of n = 2<sup>n</sup>
