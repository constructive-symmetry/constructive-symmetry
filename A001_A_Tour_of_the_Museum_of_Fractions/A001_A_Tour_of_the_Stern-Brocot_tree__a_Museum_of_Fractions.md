# A tour of the Stern-Brocot tree, a Museum of Fractions

The Stern-Brocot tree is an idea in math.[^motivation] It is like a Museum of Fractions that you can visit in your mind. An example of a fraction is one half, which is written as one over two, and is halfway between zero and one.

All the positive fractions, which are the all the fractions bounded between zero and infinity, can be found somewhere inside this museum.

These boundaries also appear as fractions guarding the sides of the front door of the museum.

To the left of the front door, zero is written as the lower boundary fraction zero over one.

To the right of the front door, infinity is written as the upper boundary fraction one over zero. [^infinity]

On the front door is written the symbol of the mediant. It looks like a fraction of plus signs, plus over plus. [^mediant]

To open the front door, first, we add across the top: zero plus one equals one. Then we add across the bottom: one plus zero equals one.

As the door opens, we see the fraction one over one,  also known as one, sitting in the middle of its room.

When the door fully opens, we see two more doors with the symbol of the mediant, a door to the left and the other to the right of one over one.  The boundary fractions get copied into the front room:  zero over one is repeated to the left of the left door, and one over zero is repeated to the right of the right door. 

All the fractions between zero and one can be found somewhere behind the left door.  All the fractions between one and infinity can be found somewhere behind the right door.

Both doors lead to a new and different room, deeper inside the museum.  However the fraction we've just seen will never again appear in the middle of another room.

To open the left door, we take the mediant of its boundary fractions, zero and one.  Adding across the top, zero plus one is one.  Adding across the bottom, one plus one is two.  As the door opens, we see the fraction one over two, also known as one half, sitting in the middle of its room.

To open the right door, we take the mediant of its boundary fractions, one and infinity.  Adding across the top, one plus one is two.  Adding across the bottom, one plus zero is one.  As the door opens, we see the fraction two over one, also known as two, sitting in the middle of its room.

The boundary fractions get copied into the rooms we have just opened, same as before.  The middle fraction is to the right of the left door, so it becomes an upper boundary fraction in the left room.  It's also to the left of the right door, so it becomes a lower boundary fraction in the right room.

The two rooms we just opened each have two doors, for a total of four unopened doors. I'm going to open all four doors.  The leftmost unopened door leads to all the fractions between zero and one half.  We open the door to find one over three, or one third.  The next door leads to all the fractions between one half and one.  We open the door to find two over three, or two thirds.

The next door leads to all the fractions between one and two, so we open the door to find three over two, or three halves.  The rightmost door leads to all the fractions between two and infinity, so we open the door to find three over one, or just three.

In this garden of forking paths, the paths downward into the museum never ever come back together.

No two doors lead to the same room, so behind each unopened door is a unique room we have not seen before.  That room has two unseen doors, therefore every time we open a door, the number of unopened doors increases by two, in addition to decreasing by one for door we opened.

Two minus one is one, so the net effect is that the number of unopened doors increases by one.  I had four unopened doors, and then I opened all four doors, so now I have eight unopened doors.  After I open those eight doors, I will have sixteen unopened doors.  And if I open those sixteen doors, I will have thirty-two unopened doors!

Two minus one is one, so the net effect is that the number of unopened doors increases by one.  I had four unopened doors, and then I opened all four doors, so now I have eight unopened doors.  After I open those eight doors, I will have sixteen unopened doors.  And if I open those sixteen doors, I will have thirty-two unopened doors!

Exploring one entire level of the museum before going deeper, like I am doing right now, is an example of a breadth-first search.  Breadth-first search is a very important idea in computer science, math, and learning.

A breadth-first search is a good way to learn what the museum looks like, because it doesn't skip any rooms.  Because of this fact, and the fact that the Stern-Brocot tree contains every fraction exactly once, we can find any fraction we want by exploring the museum long enough with a breadth-first search.

But if we are looking for a specific fraction, a breadth-first search is very inefficient because it creates a lot of unnecessary work. It is a lot less work to walk directly to the room containing that fraction, only moving down and left, or down and right. That would be an example of a depth-first search.

Depth-first search is another very important idea in computer science, math, and learning. These searches can skip rooms entirely,  which can make depth-first search efficient for finding something specific.

In my next video, I will show you how to efficiently find the room of any specific fraction, using the Euclidean Algorithm as a guidebook to the museum of fractions that is the Stern-Brocot tree.

[^motivation]:
    One of my more eccentric beliefs is that the Stern-Brocot tree should be introduced as gently as possible and as soon as possible to young children, soon after they develop a notion of counting and addition of small nonnegative integers.  Note the most difficult addition problem in this whole video is 2+3=5. (!) My guess is that this should be introduced shortly after introducing the number line, another fundamental mental model in arithmetic and geometry.  I believe this because the Stern-Brocot tree is a useful, concrete example and teaching device across a surprisingly wide swath of mathematics from elementary school all the way through postgraduate studies and beyond.  It has a uncanny knack for tying together fundamental and widely useful concepts in seemingly disparate areas of computer science and mathematics, and an uncanny knack for appearing to the solutions of problems in the most suprising ways.

    On the other hand, I am probably not the first person to ever hold this eccentric belief, judging from Neil Calkin and Herbert Wilf's classic paper, Recounting the Rationals.  See historical notes[^history], a note on mechanical engineering[^mechanical], related concepts[^related], and credits[^credits] below.

[^infinity]:
    Infinity is a weird and tricky concept, and we need to be careful what we say about it and how we use it.  Strictly speaking, infinity is not a fraction, 1/0 is not a fraction, and the pseudofraction 1/0 is not necessarily the same thing as infinity.  Keep in mind that this lesson uses the pseudofraction 1/0 only as a "boundary" fraction;  it never appears in the middle of its own room, and it's not one of "all of the positive fractions" that are greater than zero and _strictly less_ than infinity.  

    However, in the context of boundary fractions on the Stern-Brocot tree, it works to equate infinity with the pseudofraction 1/0.  This equivalence might not work out nicely in other contexts.  One or both the concepts of 1/0 and infinity may fail to make any sense in other contexts.  Even if they both make sense, they may or may not correspond to each other.

    While we can take the mediant of the pseudofraction 1/0 and another fraction,  we cannot properly add the pseudofraction 1/0 to any other fraction. Expanding 1/0 will always leave zero in the denominator, thus it is impossible to write 1/0 in like terms with any fraction.

[^mediant]:
    The mediant is sometimes known as "the wrong way to add fractions".  While the mediant is certainly not addition, the mediant is not inherently _wrong_: rather, when used in appropriate contexts, the mediant is _useful_.

    By (1) teaching the name "mediant", (2) giving the mediant a symbol that differs from the plus sign, and (3) studying how the mediant can be useful, I hope that students learning how to add fractions will more easily remember that the mediant is not addition.

    Introducing the mediant also sets up a later lesson about well-definedness, as the mediant is an example of a useful function that is not a well-defined function of fractions.  This contrasts nicely with addition, which is a well-defined function of fractions.  Learning modular arithmetic well, largely comes down to fully owning and utilizing the concept of well-definedness.

[^history]:
    The Āryabhaṭīya is a Indian text on astronomy and mathematics written in Sanskrit circa 499 CE.  It attempted to find solutions of the linear diophantine equation Ax = By + C,  for positive A, B, C, using a solution that, although the method itself seems unclear to scholars who have worked on or from English translations, seems clearly related to continued fractions. Linear diophantine equations can indeed be solved using continued fractions! The Stern-Brocot tree is essentially equivalent to the modern notion of "simple continued fractions".

    However the Stern-Brocot tree is conceptually easier to grasp for the first time, and can be used to motivate learning about integer multiplication and division, which in turn leads to simple continued fractions.  Moreover, the Stern-Brocot tree continues to be a useful mental model for simple continued fractions even after a student of mathematics starts to understand continued fractions.  The Indian mathematician Srinivasa Ramanujan (1887-1920) is particularly famous for his understanding of continued fractions, and various generalizations thereof.

    Euclid's Elements (circa 300 BC) contains a clear description of the Euclidean Algorithm, which turns out to be a guidebook to the museum of fractions that is the Stern-Brocot tree.  Knowledge of the Euclidean algorithm was expected of some 19th century British schoolboys, though it's fallen largely out of favor over the last 100 years or so, at least for classes outside of computer science and discrete math.

    The Āryabhaṭīya and Euclid's Elements were among the first Greek and Indian mathematical texts translated into Arabic circa 820 CE by the Persian mathematician al-Khwārizmī working at the House of Wisdom in Baghdad, Iraq, as part of the Translation Movement of the Abbasid Caliphate.   The Āryabhaṭīya is a major source for al-Khwārizmī's highly influential textbooks on arithmetic including "al-ḥisāb al-hindī", or the "Book of Indian Computation".  While those textbooks have been lost, they were the basis for a number of Latin textbooks on arithmetic, most famously by Fibonacci, Sacrobosco, and Christopher Clavius.

    These Latin textbooks popularized Hindu-Arabic place-value arithmetic in Europe during the late middle ages and early Renaissance, which in turn gave rise to the most widely used methods used to write down and calculate with numbers used by humans today.  al-Khwārizmī is much better known for his (still intact) textbook, "algebra", or rather "The Compendious Book on Calculation by Completion and Balancing".  The very word "algebra" is a medieval latinization of part of the Arabic name of this textbook, al-Kitāb al-Mukhtaṣar fī Ḥisāb al-Jabr wal-Muqābalah.  The word "algorithm" is also based on a medieval latinization of the name "al-Khwārizmī".

    Farey Sequences were published by John Farey Sr (1816) and Augustin-Louis Cauchy (1828), and indepedently published by Charles Haros (1802) who credited Nicolas Chuquet (circa 1480) for the mediant-based algorithm.  The Farey sequences are an inorder traversal of a finite subgraph of the Stern-Brocot tree.  Farey sequences of increasing order would be an example of iterative deeping.  Iterative deepening is an important heuristic in machine learning and human learning, and should often be preferred to breadth-first search.  Jérôme Franel and Edmund Landau proved that certain statements about the asymptotic behaviors of Farey sequences of increasing order are equivalent to the Riemann Hypothesis.  Solving the Riemann Hypothesis is one of the million-dollar Millenium Prize Problems of the Clay Mathematics Institute.

    Continued fractions (or various generalizations thereof) appear in the writings of Rafael Bombelli (1572), Pietro Cataldi (1613), John Wallis (1695), Leonhard Euler (1737, 1748), Johann Lambert (1761), Joseph-Louis Lagrange (1768,1770),  Carl Friedrich Gauss (1813), Henri Padé (1892), Srinivasa Ramanujan (1920), and Bill Gosper (1972) among many, many more modern authors.  Generalizing continued fractions to complex arithmetic is a useful tool in Complex Analysis.

    "Concrete Mathematics" credits Moritz Stern (1858) and Achille Brocot (1861) for the discovery of the Stern-Brocot tree, and mentions that Hermann Minkowski presented a lecture on the Stern-Brocot representation to the International Congress of Mathematicans in Heidelberg in 1904.  Hermann Minkowski is better known for his 1907 publication of the first mathematical models that conformed to Albert Einstein's Theory of Special Relativity, now termed Minkowski spaces in his honor.  

    Moritz Stern (1807-1894) was a professor of mathematics at Göttingen University, Germany.   Moritz Stern was the first Jewish full professor at any German university who obtained the position without first converting to Christianity.  He was the first person to be promoted to Carl Fredrich Gauss's professorship after Gauss's death.  Moritz Stern was a teacher of Bernhard Riemann, who formulated the Riemann Hypothesis.  Bernhard Riemann might have anticipated the possibility that the geometry of universe is non-Euclidean, anticipating a key aspect of the Theory of Relativity.

    Achille Brocot (1817-1878) was a French clockmaker and partner in the a small clockmaking company "Brocot et Delettrez" in Paris.  The Stern-Brocot tree was used to help select gear ratios in some of their mechanical clocks.[^mechanical] Over 100 years later, in 1971 the Hafele–Keating experiment would use cesium beam atomic clocks, the most precise clocks available at the time, to directly test time dilation predictions of the Theory of Relativity for the first time.

[^mechanical]:
    It is true that the Stern-Brocot tree leads to all the "best" rational approximations of some target.  However, the exact particular notion of "best" that corresponds to the Stern-Brocot tree is too simplistic for the purposes of selecting gear ratios in mechanical engineering.

    In this context, a "best" rational approximation is any fraction that either has a smaller denominator, or is closer to the target, than any other fraction.  Performing a binary search on the Stern-Brocot tree will lead you past every single fraction that is a "best" rational approximation, though not every fraction you pass by will be a "best" rational approximation.

    This notion of "best", while of great importance in mathematics, is too simplistic to always be directly relevant to approximating gear ratios in mechanical engineering. In mechanical engineering, a reasonable rule of thumb is that a gear should typically have less than about 100 teeth. Any more than that, and the teeth get very tiny, which can compromise mechanical strength, or the gear starts getting very big and heavy. Not to mention the manufacturing expense of such a complicated gear with more than 100 teeth! It's often better to find an approximation of the desired gearing ratio as a gear train of 2-4 links.
    
    For a more in-depth look at these issues, I highly recommend the article ["Stern-Brocot Tree and Gearing" on the Engineering Commons website](https://www.engineeringcommons.org/stern-brocot-tree).

[^related]:
    Topics that the Stern-Brocot tree relates to each other,  or are closely related to the Stern-Brocot tree, or the Stern-Brocot tree could at least serve as a useful MacGuffin for discussion,  include but are not limited to:

    1. Elementary Arithmetic 
        * integer multiplication as repeated addition
        * integer division as repeated subtraction
        * units of measurement, unit fractions, like terms
        * unit conversions, expanding fractions, adding fractions
        * comparing fractions
        * rounding fractions
        * reducing fractions, least terms
        * the Euclidean algorithm
    2. Euclidean Geometry, Linear Algebra
        * the number line
        * the golden ratio
        * Cartesian coordinates
        * slope, rates of change
        * the parallelogram law of vector addition
        * 2x2 matrix multiplication
        * determinants of 2x2 matrices
    3. Computer Science
        * binary numbers
        * binary trees
        * loop invariants
        * loop variants, halting
        * breadth-first search
        * first-in, first-out (FIFO) queues
        * depth-first search
        * last-in, first-out (LIFO) stacks
        * binary search
        * inorder traversals
        * backtracking
        * stack-based recursion
        * iterative deepening
        * run-length encoding
        * off-by-one errors
        * algorithmic complexity
        * worst-case analysis
        * asymptotic analysis
    4. Discrete Mathematics
        * Cantor's countably infinite versus uncountably infinite sets
        * Fibonacci numbers
        * relative primality
        * well-defined functions
        * well-defined relations
        * modular arithmetic
        * (co)recursion and (co)induction
    5. Calculus
        * limits, convergence of sequences
        * the (semi-)convergents of a real number X
    6. Numerical Analysis
        * continued fractions
        * dynamical systems
        * Diophantine approximation
        * best rational approximations
        * Euler-Lagrange theorem of periodic continued fractions
        * Liouville Numbers, Transcendality
        * Dirichlet Approximation Theorem
        * Hurwitz's Theorem (of Number Theory)
        * Thue-Siegel-Roth Theorem
        * exact real arithmetic
        * approximate rational arithmetic
    7. Number Theory, Cryptography
        * Farey sequences
        * the Stern-Brocot representation
        * linear Diophantine equations    
        * Pell's Equation
        * Bezout's Identity
        * the extended Euclidean Algorithm
        * multiplicative modular inverses
        * the Calkin-Wilf tree
        * finite fields
        * elliptic curves
        * modular forms
    8. Non-Euclidean Geometry, Abstract Algebra, and Complex Analysis
        * Linear Fractional Transformations
        * The Stern-Brocot free monoid SL(2,N)
        * The modular group PSL(2,Z)
        * The special linear group SL(2,Z)
        * The general linear group GL(2,Z), the automorphisms of the additive group Z⨯Z 
        * The projective general linear group PGL(2,Z)
        * The isometries of the hyperbolic plane, PGL(2,R)
        * The Möbius transformations PGL(2,C) = PSL(2,C)
        * Minkowski spacetime, Einstein's special relativity
        * Mathematical Physics

[^credits]:
    The primary influences on this video are:

    Gibbons, Jeremy & Lester, David & Bird, Richard. (2006). Functional Pearl: Enumerating the rationals. J. Funct. Program.. 16. 281-291. 10.1017/S0956796806005880. 

    Calkin, Neil & Wilf, Herbert. (2000). Recounting the Rationals. American Mathematical Monthly. 107. 10.2307/2589182. 

    Graham, Ronald & Knuth, Donald & Patashnik, Oren. (1994). Concrete Mathematics: A Foundation for Computer Science (2nd. ed.). Addison-Wesley Longman Publishing Co., Inc., USA.

    Project Euler https://projecteuler.net