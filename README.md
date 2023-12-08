This respository explicates [_an Aggregate Theory of Concrete Mathematics_](./T002_Tools_of_Math_Construction/An_Aggregate_Theory_of_Concrete_Mathematics.md). It is a philosophy of math and computer science education with practical aspirations on the elementary (K-6) curriculum, and beyond.

In addition to these materials, I highly recommend taking a look at the [National Centre for Computing Education](https://computingeducation.org.uk/), the [Brown University Bootstrap Project](https://bootstrapworld.org/), Chris D Smith's [Code World](https://code.world), as well as [Raspberry Pi](https://www.raspberrypi.org/) and [Arduino](https://arduino.cc).

Currently, this repository contains several different media assets.

The **praxis tracks** are intended to be a part of an actual course of study.  I hope that each project helps you develop a deeper understanding of some important little nugget of knowledge, but math is not a spectator sport.  To really understand something in math, you also have to play with the idea for a while.

Every folder is is intended to become a video, and to be accessible to as broad an audience as possible, especially young children.  None of these projects are quite ready to go, at the moment.  They are still under construction.

**A001** is [_A tour of the Stern-Brocot tree, a Museum of Fractions_](./A001_A_Tour_of_the_Museum_of_Fractions/A001_A_Tour_of_the_Stern-Brocot_tree__a_Museum_of_Fractions.md). This is an introduction to the Stern-Brocot tree. Currently, I have a script with detailed historical notes, a recording of my voice as an [audio track](A001_A_Tour_of_the_Museum_of_Fractions/A001_A_Tour_of_the_Stern-Brocot_tree__a_Museum_of_Fractions.flac), some [closed captions](A001_A_Tour_of_the_Museum_of_Fractions/A001_A_Tour_of_the_Stern-Brocot_tree__a_Museum_of_Fractions__CloseCaptions.txt), and an attempt at an [opening SVG graphic](./A001_A_Tour_of_the_Museum_of_Fractions/Museum_of_Fractions.svg).

I don't have video available yet to go along with the audio, and the historical notes should include more references to follow up on specific claims.

**A002** is [_The Euclidean Algorithm as a guidebook to the Museum: rebuilding fractions using the Stern-Brocot Tree_](./A002_The_Guidebook_to_the_Museum_of_Fractions/A002_The_Euclidean_Algorithm_as_the_Guidebook.md). This introduces the connection between the Euclidean Algorithm and the Stern-Brocot tree.  We start with the Pi Day approximation 3.14.  Then we use the Euclidean Algorithm to first round 3.14 ≈ 22/7, and then to finish reducing to least terms, 3.14 = 157/50. This Pi Day approximation happens to be a shadowed semi-convergent of 𝜋.  It is overshadowed by the previous convergent, 22/7, which is closer to 𝜋 despite the fact that the denominator 7 is much smaller than the denominator 50. However, as a semi-convergent, 3.14 is never overshadowed by any rational approximation of 𝜋 other than the previous convergent of 𝜋.

The script feels workable and nearly complete. There are extensive footnotes.

**A???** is an introduction to rational arithmetic, rational approximation, continued fractions, the Stern-Brocot tree as 2⨯2 matrices, deeper looks into convergents and semi-convergents, [Ford Circles](https://www.youtube.com/watch?v=0hlvhQZIOQw), [an intuitive and informal Dirichlet's Approximation Theorem](https://www.youtube.com/watch?v=uFWJuZQLKJs), [the Sail of a real number m](https://link.springer.com/book/10.1007/978-3-662-65277-0), and more.

**B???** an introduction to boolean logic, recursion, computer programming, deductive reasoning, and naive set theory. Longer term goals include backtracking, proof by induction, transitive closures, depth-first searches, binary search, preorder, inorder, and postorder traversals, breadth-first searches, and iterative deepening.

**C001** is an introduction to Pascal's Triangle. This project is the least developed of the scripts that have been started. There's a very incomplete script in there.

**C???** an introduction to counting, chance, and inductive reasoning, starting with Pascal's Triangle, path generation, the binomial coefficients, and moving towards probability and statistics, generating functions, the Integer-Valued Polynomials, and hypergeometric summation.

**D001** is an introduction to the concept of symmetry in a geometric context, focusing on the Euclidean isometries exhibited by the letters `H`, `O`, `M`, and `E`.

**D002** is an introduction to the Symmetry Group of the Square.  _Kevin Bacon and the Stern-Brocot Tree_ happened to provide a very good start on a [script for this video](./D002_Book_of_Algebra/script.md). This project includes a [mechanical calculator](D002_Book_of_Algebra/d4calculator.pdf) (also in [a4](D002_Book_of_Algebra/d4calculator-a4.pdf)): print this PDF file front-to-back, and then cut out four identical calculators by cutting along the lightest lines. It also includes some sample worksheets ([Commutativity #1](D002_Book_of_Algebra/d4-commutative-fake.pdf),[Commutativity #2](D002_Book_of_Algebra/d4-commutative-real.pdf),[Associativity](D002_Book_of_Algebra/d4-assoc.pdf))

**D003** is a focused discussion of associativity and commutativity.

**D004** [introduces a semidirect product](D004_Semidirect_Product/script.md) via the symmetry group of the square

**D005** [introduces 2⨯2 matrix multiplication](D005_Matrix_Multiplication/script) via the symmetry group of the square, likely needs to be broken up into multiple lessons.

**D006** introduces permutations via the symmetry group of the square

**D007** Discuss commutativity in more detail. The Stern-Brocot free monoid SL(2,N) never commutes, resulting in a tree structure isomorphic to binary strings.  The paths downward into Pascal's Triangle always commutes, resulting in a chessboard lattice pattern covering the first quadrant, isomorphic to the monoid N⨯N. The Symmetry Group of the Square is sometimes commutative, and can be laid out as two interconnected rings, each running counter to the other's direction.  This dihedral construction is an example of a semidirect product.  Try to work in hints of commutators, commutator subgroup, and topology.

**D???** Deeper investigations into dihedral groups, algebra and geometry.

One issue I see here already is that I really need to move this to a wiki structure, because these lessons should really be thought of as a graph, not as four lines of thought.  This ordering is both overly restrictive in this ordering already suggests false dependencies, and worse it's also insufficient because it doesn't emphasize the deeply interconnected nature of this web of ideas.

A major precipitating event in this effort is that I once overheard Edward Kmett using a metaphor of exploring a map to explain the heuristic merits of iterative deepening, as a means for both human and machine learning.

I realized I had overlooked a few things about the learning process, but I also realized I had been trying to create a much better map of elementary mathematics my entire life. The goal of this effort is to create a really good map for breaking through common mental logjams so that this material may be learned more efficiently. In a way, this repository is trying to build a royal road to mathematics.

The **theory track** is more like a series of travel brochures: these projects are trying to convince you to go learn something for yourself.  In contrast to the praxis tracks, nobody is expected to really directly understand much of anything from watching or reading these projects for the first time. Instead they are intended to provide referential knowledge, suggestions, ideas, hints, and clues about what to study next.

**T001** is [_Kevin Bacon and the Stern-Brocot Tree: a Sermon on Rational Approximation_](./T001_Kevin_Bacon_and_the_Stern-Brocot_Tree/a_Sermon_on_Rational_Approximation.md), an overview of symmetry and rational approximation, both in the sense of John von Neumann and Herbert Simon, as well as Diophantus of Alexandria. It spends most of its time on an outline of an extended course of study that starts with the Stern-Brocot Tree and the Symmetry Group of the Square, and ends with the Stern-Brocot free monoid SL(2,N), and the modular group PSL(2,Z).

This project is intended to become a video. I feel like the script is more-or-less complete. Work on the video has yet to begin. A personal intellectual history of these ideas as well as pointers for further study can be found in a tribute to [Linear Algebra and Dr. Elizabeth Meckes](./T002_Tools_of_Math_Construction/Part03_Aggregate_Theory.md), which is part of the Tools of Math Construction.

**T002** is [_Tools of Math Construction: an Aggregate Theory of Concrete Mathematics_](./T002_Tools_of_Math_Construction/An_Aggregate_Theory_of_Concrete_Mathematics.md) is study guide associated with Kevin Bacon and the Stern-Brocot Tree. It is quite long, it is semi-autobiographical, it is occasionally unpolished, and is far from complete, but I hope it will be interesting and useful in its present form. A big thank you to [Existential Comics](http://existentialcomics.com) and [XKCD](https://xkcd.com/) for the comics liberally infused into the study guide.

The **theory track** attempts to explain why the aggregate theory is the way it is. It attempts to provide a preface and 10,000 foot overview of the larger theory. It is aimed at a "prosumer" mathematical audience. I try to keep things as simple and accessible as possible, but it's also moves quickly. You aren't expected to immediately understand very much of what I mention.

Rather, the theory track is intended to create referential knowledge in the minds of students who are so interested and motivated.  These references are intended to provide hints, clues, and suggestions about places to go next.  The theory track is also intended to help teachers navigate the larger aggregate theory.

In preparation for the theory track,  I recommend being able to understand what a metaphor is, because I'm going to introduce a lot of metaphor that you won't be familiar with at first.

The metaphor-heavy nature of these projects likely means that most young children are likely to have great difficulty understanding them. Rather, these projects are more directly intended for their parents, teachers, and caretakers.

However, once a child starts to appreciate metaphor, I hope that they can derive direct benefit from the theory track.  Of course, the child may be likely to understand less than an adult, but an adult is also more likely to feel like they don't understand, and are more likely to allow their discomfort to prevent them from trying.

It's okay to feel discouraged or intimidated when trying to learn something new, but it's important to try and then try again anyway. This stuff is difficult to learn for the first time! Neither failure nor the fear of failure should prevent you from repeatedly trying to learn.

Every mathematician struggled to understand things. Many mathematicians develop a taste for the struggle, striving for the mental rush that comes from coming to a new understanding, which you grow to suspect might just be a few more failed attempts away.
