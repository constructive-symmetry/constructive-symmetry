# The Book of Algebra: The Symmetry Group of the Square

In order to understand a symmetry, sometimes you have to break it.  Start with a square piece of paper that is blank on both sides, like a book of algebra that is perfectly square.   Imagine a window over the 12 o'clock position on the book cover.  Draw a square in that window.  We'll call that square "the home square", and when the home square is in the 12 o'clock window, we'll say the piece of paper is in "home position".

Now, open the book.  Starting in home position, imagine the spine of an open book, running up and down vertically through the middle of the paper.  Now, flip the paper right-to-left around that vertical axis, almost like you were turning a page in that open book.  In the now-blank memory window, draw a square with a line down the middle for the spine.  The paper now remembers you opened it like a book.  Close the book by flipping the paper right-to-left around the vertical axis once more,  and double check that we are back in home position.

Next, rotate the paper 90 degrees clockwise, like the home square is an hour hand that now points to 3 o'clock.  The 12 o'clock window is now blank, so in the memory window we'll draw a square with a curved arrow pointing 90 degrees clockwise.  The paper now remembers how it got here, that you turned it 90 degrees clockwise away from home position.   Turn the paper back 90 degrees counterclockwise, and verify you are back in home position.

Repeat this process for the other three flips:  starting in home position, open the book like a legal-style notepad,  and flip the paper up-to-down around the horizontal axis.  Draw a memory in the window, a square with a horizontal line through it,  and then close the notepad using one smooth flip to get back to home position.  Then do the same for the two diagonal flips, and then for the other two rotations.   After you are done, you should have 8 depictions, one for each symmetry of the square, four on each side of the paper.

Our paper square, a Book of Algebra, is now a mechanical calculator for the symmetry group of the square.  It remembers all of its positions, and you can read its memory by looking at the window over the 12 o'clock position.  We can add two symmetries together by starting at home position, then performing each action on the paper square.  The paper then tells us what the net effect of those two actions put together is, by reading the memory in window.  At this point, if a student can figure out the visual pun behind each glyph and perform that action on the calculator as a whole, then the student can compute the arithmetic of the symmetry group of the square, with the help of this mechanical number line.


# Using symmetry to teach elementary mathematics

In order to appreciate a symmetry, sometimes it really helps to break it.  Consider the commutativity laws for integers, fractions, and decimal numbers.   Many students struggle to understand why commutativity is not self-evident,  and D4 is a simple example that helps break through that mental block.  In the arithmetic of D4, x + y is not always equal to y + x,  and thus addition on D4 is not commutative.  Thus commutativity is not a mere tautology.

Many students struggle to distinguish associativity and commutativity as fundamentally different things, because the examples they are taught are both associative and commutative.  D4 is among the simplest examples of a group that is associative but not commutative.  Of course, there are examples of binary operators that are commutative but not associative, and neither commutative nor associative, and all four quadrants have ideas well worth knowing.  D4 and boolean logic are two of the simplest topics that together cover all four quadrants.  Boolean logic is an essential substrate for computer programming, digital logic engineering, mathematical reasoning, analytical philosophy, and statistics.

In order to appreciate a symmetry, sometimes you have to understand it in terms of another.   Many students struggle to connect the commutatitivy of multiplication on integers, fractions, and decimal numbers to the fact that rotation of a rectangle doesn't change it's area,  and struggle to connect associativity to the fact that the rotation of a brick doesn't change it's volume.  This approach to teaching D4 should help here, too, as this provides a simple concrete mental model for the Euclidean isometries these explanations depend upon.

At some point, we should learn how to compute the arithmetic of D4 without the help of our mechanical number line.  Imagine a car on a circular track.  There are 4 stops around the track, at the 12 o'clock, 3 o'clock, 6 o'clock, and 9 o'clock positions.  In a single instruction,  you can tell the car to drive forward any number of stops, and then after the car stops, the instruction specifies whether the car turns around to change direction for the next instruction, or if instead the car continues on the same direction around the track.

Arithmetic on this representation computes the combined effect of two of these instructions.  This provides simple, concrete example of a semidirect product and a modular arithmetic, and illustrates that the dihedral introduces a hystersis of orientation.  I would probably start with this implementation.

The second implementation of D4 is based on matrix multiplication.  I cannot imagine a simpler or more ideal setting for gently introducing and motivating matrices and quickly tying their arithmetic to a memory tripod than the symmetry group of the square!   The first step is understanding D4's action on the cartesian coordinate grid Z⨯Z.   The second step is learning to implement D4's action on Z^2 by multiplying a 2⨯2 matrix with a 2⨯1 vector.   Finally, the third step is learning implement arithmetic on D4 as a full 2⨯2 matrix multiplication.  The determinant of these matrices is ±1, which corresponds to the orientation.  Linear algebra and geometric interpretations thereof certainly are topics that are easy to underappreciate, and this pedagogical route emphasizes this connection from the very start.

# Expecting the unexpected surprise

When I first started drawing the D_4 calculator on paper for the first time, something about the principles I couldn't quite articulate but was committing to in order to develop the visual pun, gave me a strong sense that I would find an unexpected reward for my expense.  I was expecting the unexpected, and then I found it: after I finished, it didn't take me long to observe that by mentally moving the "window" on this book of algebra from the 12 o'clock position to the 3 o'clock position, the calculator works flawlessly, even though different physical glyphs are involved on the obverse side!  Try it!

##  Basic examples of mathematical operators of two parameters

|                 | Commutative             | Not Commutative                           |
| --------------- | ----------------------- | ----------------------------------------- |
| Associative     | addition                | Q8, the quaternion group                  |
|                 | multiplication          | D4, the symmetry group of the square      |
|                 | vector addition         | matrix multiplication                     |
|                 | boolean and gate        | string concatination, free monoids        |
|                 | boolean or gate         | the Stern-Brocot representation, SL(2,N)  |
|                 | boolean xor gate        | the general modular group,  GL(2,Z)       |
|                 | boolean xnor gate       | S_n, the permutation group of n elements  |
|                 | Z_n, modular arithmetic | S_6, the permutation group of 6 elements  |
|                 | abelian groups          | non-abelian groups                        |
| Not Associative | boolean nand gate       | subtraction                               |
|                 | boolean nor gate        | division                                  |
|                 | absolute difference     | exponentiation                            |
|                 | average of 2 numbers    | boolean if-then implication               |
|                 | rock-paper-scissors     | boolean and-not counterexample            |
|                 | tetheral quasigroup     | function types                            |
|                 |                         | abstract syntax trees                     |
|                 |                         | Dih(G) for non-abelian group G            |
|                 |                         | octonions                                 |

addition, multiplication, subtraction, division, exponentiation on Z, Q, R, C (and quotient algebras thereof)

# Symmetry Group of the Square

* Basic Algebra

    * D4 is not commutative, commutativity is not trivial or tautological

    * D4 is associative, associativity is not the same thing as commutativity

    * D4 among the simplest concrete examples of a non-abelian group

    * Rotating a rectangle conserves area, commutativity of multiplication

    * Rotating a brick conserves volume, associativity of multiplication

    * implement D4 as a car on a circular track with four stops

    * our first concrete examples of a:

        * semidirect product, Z_4 ⋊ {+,-}

        * modular arithmetic (mod 4)

    * generalizing to D_n, and Dih(Z)

    * dihedral operator adds a hysteresis of orientation

* Geometry, Linear Algebra

    * cartesian coordinates, x-axis, y-axis

    * linear transformations, rotations, trigonometric addition formulas

    * D4 ≅ ({+,-} ⨯ {+,-}) ⋊ S_2

    * group action of D4 on Z⨯Z

    * implement D4's action as multiplication of 2⨯2 matrix with 2⨯1 vector

    * implement addition on D4 as 2⨯2 matrix multiplication

    * determinants and orientation

    * general linear transformations of the plane  GL(2,R)

    * euclidean isometries of the grid,  Z^2 ⋊ D4

    * affine transformations of the plane,  R^2 ⋊ GL(2,R)

    * homogeneous coordinates, augmented matrices

    * 3x3 matrix multiplication

    * General Linear Groups

    * Projective Geometry

* Trigonometry

    * cartesian coordinates, real-axis, imaginary-axis

    * matrix arithmetic

    * rotations

    * complex arithmetic

    * unit circle

    * euler's identity, trigonometric addition formulas

    * exponentials and logarithms

* Euclidean Isometries

    * Symmetries of Regular Polygons

        * generalized dihedral operator, Dih(Z) = Z ⋊ {+,-}

        * Dihedral Groups D_n ≅ Dih(Z_n)

        * Modular Arithmetics Z_n = Z / nZ

        * Quotient Algebras

        * Dih(G) is not associative for non-abelian G

    * Symmetries of the Line ≅ Dih(R)

    * Symmetries of the Circle ≅ O(2) ≅ Dih(R / 2𝜋Z)

        * Chaotic Dynamical Systems

    * Symmetries of the Plane ≅ R^2 ⋊ O(2)

    * Symmetries of the Cube, m3m

        * octahedral group, O_h ≅ {+,-}^3 ⋊ S_3

        * chirality, determinants

        * wreath product  O_h ≅ {+,-} ≀ S_3

            * D4 ≅ {+,-}^2 ⋊ S_2 = {+,-} ≀ S_2

            * Lamplighter Group {+,-} ≀ Z

    * Symmetries of 3D Euclidean Space ≅ R^3 ⋊ SO(3)

* Abstract Symmetries

    * Algebraic properties, e.g.

        * commutative

        * associative

        * distributive

        * morphisms

    * Permutations as Symmetries as Isomorphisms of Sets

        * bijections, 1-1 correspondence, 1-1 and onto functions

        * symmetric group S_n,  permutation group

        * permutations, factorial

        * combinations, binominal coefficients, Pascal's Triangle

        * quotient algebras

        * Cayley's Theorem, Yoneda's Lemma

        * Cantor Equivalence, isomorphisms of infinite sets

    * Symmetries of the Stern-Brocot tree

        * loop invariants, coinduction over a coalgebra

        * breadth-first search

            * isomorphism of sets between Q and Z

            * Stern-Brocot representations, SL(2,N)

        * left-right-reciprocal is an outer automorphism

        * anti-diagonal transpose switches to Calkin-Wilf tree

    * Symmetries of Pascal's Triangle

        * swap left to right:  different room, same number

        * binomial theorem, binomial series

        * generating functions

        * integer valued polynomials

        * hypergeometric summation

    * Automorphisms of D_4

        * D_4 is isomorphic to it's own automorphism group

        * This property isn't unusual

        * D_4 and Dih(Z) are unusual examples of this property

    * General Automorphisms

        * Generalized Semidirect Products

        * Outer vs Inner Automorphisms

        * Complete Groups

        * D_4, Dih(Z), and S_6

* Non-Euclidean Geometries

    * The Stern-Brocot free monoid SL(2,N)

    * The general linear group GL(2,Z)

    * The modular group PSL(2,Z)

    * The isometries of the hyperbolic plane PGL(2,R)

    * The Möbius transformations PGL(2,C) = PSL(2,C)

* Abstract Geometries
