In the context of an undergraduate math curriculum, the Stern-Brocot tree is an example that is highly relevant to Discrete Math, Abstract Algebra, and especially Number Theory. It also seems well worth mentioning in Linear Algebra, Real Analysis, Complex Analysis, and Numerical Analysis. It may well be worth more than a mention in those classes, but I don't feel like I'm nearly as well qualified to weigh in on those classes as I am the first three.

# higher-level overview

I wrote a higher-level overview of the basic approach to Elementary Number Theory [here](https://www.reddit.com/r/math/comments/1mde7pc/what_kinda_fun_math_do_you_guys_do_which_is/n694a8k/?context=3)

Personally, I don't think that [intro courses being a grab bag of results about the integers] is entirely necessary, but it took me a long time to figure out how.

My idea is to start by introducing the Stern-Brocot tree `SL(2,N)` and the Symmetry Group of the Square `D4`,  and emphasizing the use of 2x2 integer matrices and Euclid's orchard as a geometric interpretation of ZxZ.

It turns out the general modular group `GL(2,Z)` is the Minkowski product `D4 SL(2,N) D4`, which gives enough structure to explain most of the algorithms commonly found in intro courses.

Moreover, many students coming into NT for the first time aren't particularly well versed in modular arithmetic, and D4 includes Z4. One of the challenges is appreciating the importance and power of well-definedness, and it turns out the Stern-Brocot tree depends on the mediant operator, which isn't a well-defined function over the fractions.

One of the neat things is that conducting a binary search for `a/b` on the Stern-Brocot tree is equivalent to running the extended Euclidean algorithm on `a` and `b`, giving a way of generalizing the extended euclidean algorithm to irrational numbers, and clarifying the connection between the extended Euclidean algorithm, diophantine approximation, and the real numbers.

And of course this also means that the Stern-Brocot tree is a sufficiently rich computational structure to implement all of the trickier algorithms commonly found in intro NT, from computing multiplicative modular inverses to the inverse Chinese Remainder Theorem.

# another off-the-cuff answer

I started writing down my thoughts on how I'd approach elementary number theory if I were teaching the class as a response to somebody who felt totally lost in an intro to elementary number theory type of class.  I eventually plan on expanding on and editing this note:

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

# note about relevance

Number Theory has often been held up as one of the "useless" branches of
mathematics, by no less than the likes of G.H. Hardy and others. To the extent
that was ever true, it's not true any longer. I'd like for an intro number
theory class to mention some of the surpring connections, though I probably
wouldn't spend a great deal of time on them:

1.  The moduli space of acute triangles.

    *   See in particular, see [The Moduli Space of Acute Triangles](https://www.ams.org/journals/notices/202405/rnoti-p664.pdf) by John Baez.

    *   Would the unit circle be an example of a moduli space of right
        triangles? I'm not familiar enough with the concept of moduli spaces
        to know all the finer print involved.

    *   Also, technically you don't need the full unit circle: 1/8 of a circle
        covers the space, but also has a "cusp" (probably not quite the right
        word) that disallows the passage of any object that cannot pass through
        itself. (But doesn't the moduli space of acute triangles have a very
        similar feature?)

    *   A quarter of a unit circle would avoid this feature, but also
        represents something about the orientation of a right triangle in
        addition to a space of all similar right triangles.

2.  Ford Circles and the Apollonian Gasket

3.  `GL(2,Z)` represents the automorphisms of the additive group `Z^2`, and
    Pick's Theorem.

    These two closely related observations might warrant a bit more than a
    simple mention in intro to NT. In particular, these facts lead to alternate
    proofs that every fraction that appears on the Stern-Brocot tree is in
    least terms. Starting with a review of the "simplest" proof:

    1.  Proof: `det [x w; y z] = 1` implies that `gcd(x,y) = 1`. Rewriting the
        determinant, we find `x*z - w*y = 1`, thus `w` and `z` bear witness to
        the fact that `gcd(x,y) = 1`. Via the symmetry, this argument also
        demonstrates that `gcd(x,w) = 1`, `gcd(y,z) = 1`, and `gcd(w,z) = 1`.
        To demonstrate that every `a/b` that appears on the Stern-Brocot
        tree is in least terms, we can use the Euclidean algorithm to calculate
        `m = [x w; y z] ∈ SL(2,N)` such that `m [1; 1]` is equal to `[b; a]`,
        and then move left or right on the tree to demonstrate that
        `[x b; y a] ∈ SL(2,N)` and `[b w; a z] ∈ SL(2,N)`, which demonstrates
        that the determinant of these matrices are equal to one, and thus
        `gcd(a,b) = 1`.

    2.  Proof: given some `m = [x w; y z] ∈ SL(2,N)`, the fact that `det m = 1`
        implies that the parallelogram defined by the two vectors `[x;y]` and
        `[w;z]` has area 1. We can use Pick's theorem to directly calculate
         that this parallelogram contains no interior lattice points, as all
         the area is accounted for in the boundary lattice points.

    3.  Proof: because multiplication by some `m ∈ SL(2,N)` represents an
        automorphism of the additive group `Z⨯Z`, we can translate the
        parallelogram represented by `m` to the unit square `[0,1]⨯[0,1]`,
        recognize that the unit square contains no interior lattice points, and
        then translate this negative answer back to our original parallelogram,
        deriving this answer via a change of basis.

        Hmm, I'm thinking that this intuition applies to two rather different
        proofs. The most direct formalization of this proof also relies on the
        fact that `m` is continuous over `Q²`. (Or do we need `R²` here?) On the
        other hand, there is a slightly less-direct formalization that can be
        made purely algebraic. Either way, we still depend on the fact that
        multiplication by `m` is an automorphism of `Z²`, which is implied by
        the fact that `m` is a `2⨯2` integer matrix and `det m = 1`.

    Actually we only need to prove that elements of `SL(2,N)` represent
    automorphisms of `Z²` for these proofs: we don't need the fact that
    any automorphism of `Z²` is represented by something in `GL(2,Z)`, i.e.
    the other half of the isomorphism between `GL(2,Z)` and `Z²`.

    The proof of the first fact should be rather straightforward for anybody
    with a basic working knowledge of abstract algebra. The proof of the second
    is vaguely less straightforward, and perhaps could be skipped because I
    don't know how it might specifically be of use in elementary number theory.

    **Theorem:** any homomorphism `f : Z² → Z²` can be represented by
    a `2⨯2` integer matrix.

    **Proof:** Given an arbitrary `[x; y] ∈ Z²` in the domain of `f`, note that:

    ```
    [x; y] = [1; 0] + ... + [1; 0] + [0; 1] + ... + [0, 1]
             |                   |   |                   |
             \----- x times -----/   \----- y times -----/
    ```

    Without loss of generality, assume `f [1; 0] = [a; b]` and
    `f [0; 1] = [c; d]`. Note that all variables must be integers, as the
    range of `f` is `Z²`. Applying `f` to both sides, applying the distributive
    property of homomorphisms, and collecting like terms, we find that:

    ```
    f [x; y] = x * f [1; 0] + y * f [0; 1]
             = x * [a; b] + y * [c; d]
             = [a c; b d][x; y]
    ```

    This is the trickiest part of a precise characterization that the
    endomorphisms of `Z²` are isomorphic to `2⨯2` integer matrices. What is
    left to prove is: that all integer matrices represent homomorphisms from
    `Z²` to `Z²`, that the mapping from `2⨯2` integer matrices to endomorphisms
    is injective, and that matrix multiplication corresponds to the composition
    of endomorphisms.

    **Theorem:** a homomorphism `f : Z² -> Z²` is an isomorphism if and only if
    it's associated matrix `m` is of determinant `±1`

    **Proof:** Note that `det m` must be an integer. If `det m = ±1`, then the
    inverse matrix `m⁻¹` is also an integer matrix, by the well-known formula
    for the inverse of `2⨯2` matrices.

    Thus `m⁻¹` represents `f⁻¹`, which must also be an endomorphism.
    Because `f ∘ f⁻¹ = id` and `f⁻¹ ∘ f = id`, we find that `f` is an
    isomorphism.

    If the determinant of `m` is `0`, then `m` represents a reduction in
    dimensionality and thus is neither injective nor surjective. If
    `|det m| > 1`, then the inverse matrix will not be an integer matrix. Thus,
    at least one of `m⁻¹ [1; 0]` and `m⁻¹ [0; 1]` will not be in `Z²`, which
    implies that the corresponding basis vector(s) do not show up in the image
    of `m` over `Z²`, and thus the endomorphism defined by `m` is injective but
    not surjective.

    A collarary is that `Z²` does not admit any endomorphisms that are
    surjective but not injective. This completes a finer-grained
    characterization of all the endomorphisms of `Z²`.

    Another perspective is that these observations are implied by the facts that
    `det (x * y) = (det x) * (det y)`, that integer matrices have integer
    determinants, and that the only integers with multiplicative inverses are
    `±1`. Once the absolute value of the determinant is greater than one, you
    cannot multiply by an integer matrix to reduce the absolute value of the
    determinant to anything other than zero. Moreover, once the determinant is
    zero, no further matrix multiplications of any kind will ever change the
    determinant away from zero.

    Furthermore, the mapping from `GL(2,Z)` to `Aut(Z²)` is injective, because
    if `m, m'` are distinct matrices in `GL(2,Z)`, then it must be true that
    `m [1; 0] ≠ m' [1; 0]` or `m [0; 1] ≠ m' [0; 1]`, which implies that the
    associated automorphisms must differ at least one of those points and thus
    represent different functions. This completes the characterization that the
    automorphisms of `Z²` are isomorphic to `GL(2,Z)`.

4.  `SL(2,Z)` and `PSL(2,Z)` are examples of discrete models that obey the
    axioms of Special Relativity.

    See especially [This Week's Finds 14: the Three-Strand Braid Group](https://www.youtube.com/watch?v=MnS4hduP5xg) by John Baez.

5.  Much like `D_4` is a discrete subgroup of the Euclidean isometries of the
    plane, `PSL(2,Z)` is a discrete subgroup of the isometries of the
    hyperbolic plane.

6.  Connections to the three-strand braid group and to rational tangles.

7.  Modular Forms may also be worth mentioning.
