In the context of an undergraduate math curriculum, the Stern-Brocot tree is an
example that is highly relevant to Discrete Math, Abstract Algebra, and Number Theory. It also seems well worth mentioning in Linear Algebra, Real Analysis, Complex Analysis, and Numerical Analysis.  It may well be worth more than a mention in those classes, but I don't feel like I'm nearly as well qualified to weigh in on those classes as I am the first three.

In any case, I started writing down my thoughts on how I'd approach elementary number theory if I were teaching the class as a response to somebody who felt totally lost in an intro to elementary number theory type of class.  I eventually plan on expanding on and editing this note:

https://www.reddit.com/r/math/comments/17eqmc7/i_dont_know_how_to_succeed_in_math_anymore/k69l60t/

First of all, breathe.  Everything will be okay, one way or the other. In one sense, you are always in the shallow end, relative to mathematics itself.

Second, laugh. _Proofs and Refutations_ by Imre Lakatos is notable for it's use of humor.  It also contains quite a few hints at what your issue might be.  _Mathematics and Plausible Reasoning_ and _How to Solve It_ by George Polya are also good ones to turn to if you are having difficulty.  Daniel Velleman's _How to Prove It_ also has a nice concise overview of elementary number theory, and provides a structured approach to proof writing.  I would especially recommend focusing on _How to Prove It_ for now, but I would strongly recommend you at least browse the remaining books, by at least reading the preface and first chapter or so (but don't put too much effort into a first read).

Thirdly, go broader.  Take a look at the [Stern Brocot-Tree and the Symmetry Group of the Square](https://github.com/constructive-symmetry/constructive-symmetry). I would encourage you to use 2x2 integer matrix multiplication and determinants. If you are willing to try to read well-written Haskell, I strongly recommend [Functional Pearl: Enumerating the Rationals](http://www.cs.ox.ac.uk/people/jeremy.gibbons/publications/rationals.pdf). If you are comfortable writing short and simple programs, I strongly recommend trying to solve [Project Euler #192](https://projecteuler.net/problem=192).  I would suggest looking at maybe the first five chapters of "Visual Group Theory" or so. You might also take a brief look at "The Joy of Abstraction", and see what you think.  For alternative presentations of the material, you might try taking a look at Chapter 4 of "Concrete Mathematics" and H. Davenport's "The Higher Arithmetic".

Are you still thinking about everything in terms of congruences?  That is, are you still thinking about `(mod n)` as if it is attached to the logical proposition of equality?  After all, this is the first definition typically used.

However, when looking at a statement such as `a * b = 1 (mod 4)`, it's extremely helpful to conceptually think of `(mod 4)` as describing the type of the variables `a`, `b` and the literal constant `1`  _in addition to_ describing the types of the equality and multiplication operators.

The "type" of (mod 4) is often referred to Z_4 in the lingo of abstract algebra, though Visual Group Theory calls it C_4.  In this context, you assume that 0 = 4.   Unless you want to sacrifice the addition property of equality, this assumption implies

    ... = -8 = -4 = 0 = 4 = 8 = ...
    ... = -7 = -3 = 1 = 5 = 9 = ...
    ... = -6 = -2 = 2 = 6 = ...
    ... = -5 = -1 = 3 = 7 = ...

So we only end up with four "numbers" in this system, each with an infinite number of different names.   But now we need to make sure that our ability to reason algebraically hasn't been damaged by our change, which corresponds to the algebraic property of being [well-defined](https://en.wikipedia.org/wiki/Equivalence_relation#Well-definedness_under_an_equivalence_relation), which ideally should be proven.  

It's probably easier to understand what a well-defined function is, by looking at what it is not. In particular, the mediant, aka adding fractions the wrong way, is not a well-defined function of fractions.

For example, the mediant of 1/2 and 1/3 is not equal to the mediant of 2/4 and 1/3,  even though 1/2 is equal to 2/4.   Thus usage of the mediant means a certain kind of subsitution we are accustomed to making breaks down.

However, the correct addition rule for fractions is well defined: sure, using the usual algorithm you might find the name for the answer to be 5 / 6 one way, and 10 / 12 the other way, but these two names refer to the same conceptual object.   Thus addition is a well-defined function of fractions, and the mediant is not.

The next step is applying the concepts of well-definedness to integer arithmetic, and realizing that the following functions are well defined for all n:

    plus :: ( Z_n, Z_n ) -> Z_n
    mult :: ( Z_n, Z_n ) -> Z_n
    exp :: ( Z_n, Z_phi(n) ) -> Z_n
    (==) :: ( Z_n, Z_n ) -> Bool         
      where   x == y  iff  n divides (x - y)

Here, addition, multiplication, and exponentiation can be taken to be the usual algorithm on integers. However it is necessary to modify the usual equality algorithm to accommodate all the aliasing we introduced. 

Proving the above statements for addition, multiplication, and equality is fairly straightforward. Exponents are a little tricky to understand and prove for the first time, but the statement above is deeply connected to Fermat's Little Theorem, Euler's Theorem, and Lagrange's Theorem. Then Euler's Totient poses additional complications, but isn't too bad to just learn how to compute the totient from a prime factorization of n.  

The Chinese Remainder Theorem is an isomorphism of rings. It explains why Euler's Totient is a multiplicative function, and the CRT tends to arise in other contexts when you are working with multiplicative functions.  That completes the core algebraic content of the core topics typically covered in a university-level intro to number theory class.

The other particularly important aspect of getting good at elementary number theory is understanding how this algebraic view of things is related to an algorithmic view of things.  A good algorithm efficiently bears witness to the algebraic properties, ideally in both directions (if possible). The algebraic properties help you compose the algorithms together to achieve a given goal.  Algebra allows you to reason about what the result of a given algorithm would be without actually performing the calculation.  Algebra can even suggest better algorithms.

In terms of algorithms, you really only need addition and multiplication, (the ones you already know), additive inverses (i.e. subtraction), multiplicative inverses (via the extended euclidean algorithm), the understanding that well-definededness means that you can always add or subtract any multiple of the modulus at any time to find an equivalent name for the same object, efficient modular exponentiation by applying the previous observation throughout a entire computation, and the Chinese Remainder Thereom (via the extended Euclidean Algorithm), and how the Extended Euclidean Algorithm corresponds to the Stern-Brocot Tree and the mediant operator.

Once you have a reasonable initial understanding of this cluster of ideas, things will get a lot easier. Number theory is one of those things that's very difficult until you find or construct good mental models... which isn't easy the first time, but is doable. Like I said, I think you probably need to mix it up and go broader, which is generally a very useful heuristic.  This is sort of my default advice for tackling elementary number theory for the first time, if you tell me more about your experiences I would reasonably likely be able to refine or focus my advice.
