[Back to Part 2: Deconstructing Bertrand Russell](./Part02_Deconstructing_Bertrand_Russell.md#navigation). Up next, Part 3:


# an Aggregate Theory of Concrete Mathematics
## Suggestions for Further Study

* Indra's Pearls: The Vision of Felix Klein, by David Mumford, Caroline Series, and David Wright
  * A state-of-the-art introduction to computer graphics, fractals, mathematics, and much more.
  * reminds me a lot of examples from "Oh! Pascal!", but much more in-depth.
  * Like "Proofs and Refutations", this book has a similarly high potential for improving my math education, had I been able to read it in high school.
  * Chapter 7 covers modular group
  * Potentially pairs well with:
      * Chaos, by James Gleick
      * Euler's Gem, by David S Richeson
      * The Knot Book, by Colin C Adams
      * Visual Group Theory, by Nathan Carter
      * Visual Complex Analysis, by Tristan Needham
      * Visual Differential Geometry and Forms, by Tristan Needham

* Introduction to Experimental Mathematics, by Søren Eilers and Rune Johansen
  * A continuation of _the inductive attitude_ theme of this essay
      * The Scout Mindset, by Julia Galef
      * How to Solve It, by George Pólya
      * Mathematics and Plausible Reasoning, by George Pólya
      * Proofs and Refutations, by Imre Lakatos

* Concrete Mathematics (2nd Ed.), by Ronald L Graham, Donald E Knuth, and Oren Patashnik
  * Exercise 4.4: Depends on interpretation.
     * if interpreted as pair, then (1,1) /= (-1,-1), and
          * then it's four of the eight lobes of the group SL(2,Z)
          * SL(2,Z) is the transitive closure of these lobes under group multiplication.
     * if interpreted as ratio, then 1/1 == (-1)/(-1), and
          * it's two of the four lobes of the modular group PSL(2,Z), each duplicated twice
          * PSL(2,Z) is the transitive closure of these lobes under group multiplication.
     * the function \x -> x * ((0 1)(-1 0)) is a bijection between the provided lobes and the missing lobes
  * see scanned notes
  * should rewrite essay in TeX to expand on this answer.
     * a free presentation of the modular group based on pointwise product of D_4 * SL(2,N) * D_4
     * syntactic correspondence (computable by a small and simple Mealy-type finite-state machine) of the _coproduct_ (also known as the _free product_) of Z_3 and Z_2
     * include a more careful writeup of the results in my notes, alluded to in KB&SBT and the tribute that follows
  * Synthesizing this answer with "Algebra: Chapter 0" by Paolo Aluffi should be a very fertile exercise.

# An intellectual history of an Aggregate Theory
## A tribute to linear algebra and Dr. Elizabeth Meckes

I knew Elizabeth and Mark from my undergraduate days at Case Western Reserve University when we were all students. As an undergrad, I was often overly fixated on the decidedly non-linear design problems that programming languages pose, which was extremely weird for the department. I stumbled my way to a math major, and earned a computer science minor about three times over.

It was obvious to me that Elizabeth and I shared many philosophical principles of math education, and I admired Elizabeth's enthusiasm for curriculum reform. We both believe that it is important to refer to key concepts early and often. Introducing linear algebra via gentle introductions to matrix arithmetic and linear transformations are deeply baked into my theory of math education. While this emphasis on preparing students for linear algebra was not always intentional, neither is it entirely accidental. Rather, it is a byproduct of chance guided by a philosophy of design.

Linear algebra is easy to underappreciate, even if you have a reasonable understanding of it and its importance.[^graphicallinearalgebra]  In fact, developing my Aggregate Theory of Concrete Mathematics has brought deeper practical appreciations of linear algebra repeatedly over the period of many years. Linear algebra is among the grandest mountain ranges of modern mathematics, and Linear Algebra is indeed one of the most important math classes you'll ever take.

After I graduated from Case Western Reserve University, I taught some remedial algebra classes at Ivy Tech Community College for fall of 2004 and spring of 2005, and I found myself very much in want of a better way to illustrate the basic algebraic properties of associativity and commutativity. As a secondary motivation, I wanted a way to efficiently break mistaken assumptions about what numbers are, and provide a suggestive hint of what they can be.

Around that time I first read Dr. Doron Zeilberger's Opinion #65 on Gelfand's Principle, which I immediately found absolutely fascinating. It comported with my pre-existing pedagogical philosophy and also nicely elucidated it. It inspired me to go above and beyond: I wasn't content with developing one example for a few lessons. I wanted to discover examples to cover and recover many times, in a logical progression of ideas! Ideally, it could be introduced in early elementary school and extend all the way through the high school college-prep curriculum and beyond. I wanted to leave students better prepared than I was for as a diverse a selection of university-level undergraduate math classes as possible.

With this in mind, for the specific problem I was seeking to address, I wanted the simplest, most naturally motivated, most interesting example of something that was associative, but not commutative.[^nandnor]  So I thought back to my class with Dr. Dong Hoon Lee, taught from Fraleigh's abstract algebra book. I wanted a simple non-abelian group I could conceivably use. I quickly focused my attention on D_4, the symmetry group of the square, because rotating the the area of a rectangle explains why multiplication is commutative, well within the wheelhouse of the class I was planning this lesson for.[^alternatives]  In fact, these lessons could even be adjacent to each other, and hopefully reinforce each other.

I was also attracted to D_4 because of it's particularly simple action on the cartesian coordinates, which lead to particularly simple and pleasing connections to graphing equations, the unit circle, complex arithmetic, and trigonometry, all well within my longer-term college-prep target. I was keenly aware that attempting to teach D_4 the way it was taught to me, in the class I was contemplating using it in, was an absolute non-starter. So I started relearning the symmetry group of the square again for the first time.

A year or so later I demonstrated my explanation of D_4's action on the cartesian coordinates to Larry Moss. He was amused, laughed, and said "Oh you've got your linear transformations right there!"  I was struck with the force of revelation, because in my mind I had written down anonymous functions. In retrospect the connection was so blindingly obvious that I was amazed that I had overlooked it.

Yet somehow, I clearly had overlooked this connection. I almost certainly would have spotted it eventually. My introduction to matrices in Algebra II focused on row reduction and solving systems of linear equations, whereas my first deep dive into linear transformations came later in linear algebra, and I simply had not thought that far ahead in terms of curriculum implications. On the other hand, I reviewed Fraleigh (5th Edition) early on in my process of relearning D_4. I clearly remember reviewing pages 94-95, but I suspect I didn't take a close enough look at the exercises on page 96, which in retrospect seems like a significant heuristic blunder. No matter, after my interaction with Dr. Moss I made sure that linear algebra was on my hotlist of free mental associations with D_4.

One of the first things I remember Dan Friedman telling me was that whenever you write a program to do something, you should also write the program to undo that thing. I remember thinking "that's a nice idea in theory", and then my mind first raced to undoing cryptographic hash functions, and second to undoing the Euclidean Algorithm. Of course, cryptographic hash functions are specifically engineered to try to be computationally infeasible to undo, and properly appreciating the design of that kind of function requires a deep understanding of how to undo a lot of things!  But I didn't have an answer to the latter question that satisfied me, so I filed a mental note to "write a program to undo the Euclidean Algorithm" away, and promptly forgot about it.

At the time, I was well aware of the Extended Euclidean Algorithm from David Singer's number theory class, which can very reasonably be said to "undo" the Euclidean Algorithm in the sense I was looking for. However, the more obvious connection is number-theoretic. The connection to the continuum of the real number line is much less obvious, unless you are clued into continued fractions and/or the Stern-Brocot tree.[^sbt-undergraduate-retrospective]

In elementary school,  I loved the ideas that surrounded greatest common divisors and the reduction of fractions to least terms, but I hated the fiddly nature of actually doing it. Around third grade I wrote a BASIC program to reduce fractions for me. It wasn't pretty, I'm pretty sure it involved a nested loop, expressed as a bowl of spaghetti code. I clearly remember being forced to think carefully about whether to use "and" or "or" to combine boolean expressions. But it worked, and I saved it to diskette and used it as much as possible for math homework after that.

I first developed an appreciation for the Euclidean Algorithm in Grade 7, by reading a side-box blurb from a math textbook we were using. I then rewrote my fraction-reducing program with this in mind, and marvelled at how much shorter and clearer and more insightful the Euclidean Algorithm was compared to my previous mess. This was a seminal event in building my intuition for loop invariants and how to write programs well.

Around this time I recall seeing continued fractions once in a great while, never with much explanation, in what seemed to be weird disjointed contexts. Continued fractions seemed strange and incomprehensible. Little did I know that they are just the other side of the Euclidean coin, intimately connected to one of my favorite algorithms!

My first real "aha!" moment with continued fractions came from reading articles on cut-the-knot while solving Project Euler problems. I immediately realized that continued fractions are a deeply satisfying answer to the question Dan Friedman inspired. I also knew that my junior high self would have likely appreciated that explanation, and so I immediately knew I had another partial answer to the question "How to teach math?" that I had to keep track of.

Days after that, I was reading the then-recent paper "Functional Pearl: Enumerating the Rationals" by Jeremy Gibbons, Richard Bird, and David Lester. This was my first introduction to the Stern-Brocot tree and it's connection to the Euclidean algorithm and the Calkin-Wilf trees. Soon after reading that paper, I knew that the Stern-Brocot tree was one of the most important partial answers I had ever stumbled upon to "How to teach math?".

I was struck with this force of revelation for four reasons: first of all, The Stern-Brocot tree provides a very appealing mental model for thinking about continued fractions. Now I believed I could successfully introduce these ideas to my five-year old self. Being able to increase my bid from "my Junior High self" to "my 5-year old self" was _extremely_ interesting.

Second, the Stern-Brocot tree is a naturally motivated demonstration that the "wrong way to add fractions" is useful. The mediant very nicely illustrates and motivates the property of being well-defined, because it is not a well-defined "function", and this demonstrates that these "functions", while not functions in the strictest sense of the word, can still in fact be very useful, which is a wonderful thing to learn early.

Thirdly, the simplification from continued fractions to the Stern-Brocot tree nicely comported with the philosophy exemplified by Dan Friedman to first write a program in the simplest, most natural way possible, and then strive to  derive more efficient versions from that. This is something that I would probably still benefit from putting in into practice more often.

Translating this philosophy into the realm of math education, that means we can introduce the Stern-Brocot tree and the Euclidean algorithm before any discussion of integer multiplication or integer division. Then, we can connect multiplication and division to repeated addition and repeated subtraction, run-length encoding and continued fractions. Instead of spending years drilling boring multiplication and division before we get to the interesting stuff, we could go the straight to interesting stuff first and use it to motivate the introduction of multiplication and division! This is great, not least because integer division had long been a particularly fascinating nexus in my memory palace of mathematics, and now it just got far more interesting!

Fourth and finally, by the metrics of Gelfand's Principle, the Stern-Brocot tree is a naturally motivated pedogogical example for the hyperset theory I had learned about on my own from Jon Barwise and Larry Moss's "Vicious Circles" while I was at Case Western Reserve University, and the coalgebras and coinduction I later learned a bit about from sitting in on some of the lectures of Larry Moss himself at Indiana University.[^barwiselakoff]

Now, I have been deeply interested in the question "How to teach math?" since early childhood, and now I unexpectedly had four very interesting answers to four questions that were highly relevant to my longstanding interest. It was a firestorm of unexpected insight, and I felt utterly amazed for several weeks thereafter.

Life happened, and these ideas got shuffled to the backburner. In the intervening time, I attended several NYC Compose Conference organized by Ryan Trinkle and Obsidian Systems. At one of those events, perhaps at the same event where Ozgun recommended "Statistical Rethinking" in the hallway, I heard Edward Kmett talking extemporaneously to somebody else about the merits of iterative deepening as a heuristic for learning mathematics.

Now, Edward Kmett may well be the the most conventionally intelligent man I've ever met. He is a force of nature, with an astonishing breadth and depth of knowledge in mathematics and computer science, and with a level of energy and stamina that I often simply cannot keep up with. So naturally I was extremely interested in what he was saying. As I was listening to Ed talk about the way he accomplished some truly astonishing feats of personal learning, I realized Ed was, like Doron Zeilberger, touching many ideas that were in already in my own head. However, Ed was explicating instincts that were buried even more deeply in my subconcious, and also pointing out a large number of things I had never considered, even instinctively. As I listened, I knew the thoughts that he was creating in my head was a seed for an answer to the question "How to teach math?" that I had long been seeking.

I knew that if I dropped that seed into the supersaturated solution of unorganized partial answers to "how to teach mathematics" in my mind, a much better answer would start crystallizing. Finally, this pandemic, the coup, the prodding of a dear friend, and meeting the young son of a personal friend, inspired me to bring these ideas back to the forefront of my mind. As expected, the theory started getting organized. Then the theory started growing rather more vigorously than expected.

It had long been obvious that the Stern-Brocot tree would be the frontispiece of my theory. As I started planning my first videos on rebuilding fractions and the Stern-Brocot tree, I realized I couldn't quite adequately explain the connection between the Stern-Brocot tree and the Euclidean algorithm. I could explain how the connection worked, but realized I couldn't quite answer why. This was creating doubts that I would be able to give a really suggestive answer "how". So I reviewed "Enumerating the Rationals", discovered that it never actually explained the "why" of the connection, and followed the reference back to "Concrete Mathematics". In retrospect, I had been personally experiencing the knowledge illusion regarding the nature of this connection.

I quickly came to the conclusion that the current edition of Concrete Mathematics buries the lede regarding the Stern-Brocot tree. I had looked at the table of contents of "Concrete Mathematics" as an undergraduate, but sadly I had overlooked the actual content of the book until the summer of 2021. This time, I was deeply amused by the preface, as it evoked memories of a great many critiques and defenses of New Math that I've read and pondered over the years, memories of which have faded into mush, but the echoes of which are still with me in the ways they informed my philosophy of math education.

I found the section on the Stern-Brocot tree to be very nicely written overall. The connection to the Euclidean algorithm I found to be immediately clear upon a first read. Again I was struck by a force of revelation: I had again been overlooking linear algebra. This explanation is the only place in the book that uses it, which made it very clear to me that linear algebra deserves to be higher up in my mathematical toolbox.

Later, as scripts for my first two videos were starting to come together, I was thinking about how to answer the inevitable question, why should I care? I got myself into the mindset of a hype man to frame the answer, and then over the course of a couple days, I somewhat unexpectedly wrote the opening sentences to "Kevin Bacon and the Stern Brocot tree", which I've hardly touched since. Those opening lines were both a cause for, and effect of, my coalescing interest in the primary aggregates of my educational theory.  I had the starting point, the Stern-Brocot tree.

Browsing Concrete Mathematics, thinking about how to teach and motivate probability and statistics, and thinking about Paul Erdős and how to extend the metaphor of opening sentences in the best way possible, reminded me that Pascal's Triangle also needed to be a frontispiece. That in turn reminded me of a time when I was teaching Algebra I to Ivy Tech students, and I gave a very brief overview of the Binomial Theorem and Pascal's Triangle.  This felt well beyond the scope of the course, which I knew was playing with fire. And yet, the brief excursion was unexpectedly well received by a student.

Finally, I hesitantly added the Symmetry Group of the Square, not because I understood the connection; in fact I didn't at the time have the strength of conviction that this idea really deserved to be a frontispiece.  Yet, linear algebra provides a relatively "obvious" connection between these aggregates. The fact that I didn't see that linear algebra is common factor between the Stern-Brocot tree and the Symmetry Group of the Square, I find absolutely fascinating.

Coalescing on the primary aggregates was a natural consequence of enlarging the metaphor of the frame I was trying to construct. In my mind, this process of contemplating the arc of "Kevin Bacon and the Stern-Brocot Tree" and writing the opening sentences like going all-in on an auction in contract bridge, doubled and re-doubled, and now I had to figure out how to take all the tricks to make the bid.

That took a lot longer than I expected. It took several weeks to expand my opening lines into reasonable drafts of the first section about the Six Degrees of Kevin Bacon. Then it took several more weeks to start seeing reasonable drafts of my second section about Julian Gevirtz and God's Textbook of Mathematics. As that creative burst was starting to cool, I unexpectedly had one of the more memorable experiences of my life.

I happened to be surfing `/r/Arduino` on reddit, and somebody posted a picture of a binary counter they made out of 8 LEDs, with the headline "1-256" binary counter. And then somebody responded "0-255". Their obvious intention was to point out the off-by-one "error": the most canonical interpretation an 8-bit machine word would be 0-255, not 1-256. And then with playful intent, I responded, 0 = 256 (mod 256), so 1-256 works too. After all, an 8-bit unsigned machine word is (typically) isomorphic to the group of integers (mod 256), and is never isomorphic to the integers themselves. Sliding the window of modular arithmetic to 1-256 is essentially the same idea that is behind two's complement signed arithmetic. I was just offering a counter-refutation, to a perfectly insightful opening refutation.

Although my counter-refutation would not have caused anybody to bat an eye in `/r/math`,  I was aware that in `/r/Arduino` was likely to be received negatively without unpacking a lot of context. But that's time consuming, and makes it easy for others to stop reading early. Once in a great while I enjoy provoking and taking on a sterotypical embedded programmer's aggressively provincial views of what mathematics is. That part's easy for me. I was expecting a bit of a backlash, and I was expecting to defend my position, hoping that it would be fun and enlightening.

This time, the backlash was much stronger than I expected, and I was downvoted into oblivion. Another redditor, perhaps in his mind labelling me as one of those post-modern mathematicians, decided to try to prove me wrong using their superior wiki-ing skills and ad-hominem attacks.

I sparred with my opponent for a while. It quickly turned much nastier than I prefer, but I know what I know, and I do know a thing or two about math. After quite a few back and forths, as it was becoming clear that I would soon be refusing to participate in further debate, I got a notion to write one more response. And right as I posted, I thought, in the likely case he does respond, I'll take his response directly back to the Stern-Brocot tree if at all possible, and the larger Aggregate Theory if not, and then be done with this conversation.

So I posted, and I was soon treated to a response in which I was a attacked for referring to "the modular group Z_256", via a wikipedia link to "the modular group, PSL(2,Z)", arguing that this minor difference in language meant I should go back to the basics and relearn arithmetic. Well I mean, he isn't wrong. I have a copy of "Winning Ways for Your Mathematical Plays", and I would probably greatly enjoy spending time relearning arithmetic from that book.

The thing is, I don't specifically recall hearing about "the modular group, PSL(2,Z)" before this event. Reading the wikipedia article he sent me, I was immediately struck with the force of revelation, but this time looking outward from the shoulders of linear algebra. I immediately understood that the Stern-Brocot tree was somehow embedded within the modular group, because both things corresponded to 2x2 matrices of determinant one. And there was a connection to complex analysis!

I was completely lost in complex analysis, but I did take away three things, first a real admiration for Tristan Needham's "Visual Complex Analysis", secondly the beginnings of my awareness of the weaknesses and limitations of formalist mathematics,  and thirdly, having enthusiastically taken up what Sir Michael Atiyah deems the Faustian bargain that algebra offers, I realized I should have invested more into the study of geometry. In my research program for math education, finding pathways into classes where I previously had trouble, is always very interesting.

This was all very amazing!  I thanked my sparring partner for the link, and ended the conversation. I do geniunely mean that: if you are the person of whom I speak, and you ever read this, thank you!  For me myself personally, this has been the only time this kind of sparring has ever paid off in a really big way. It most certainly was a momentous experience!

I went back to `/r/math` and quipped "the modular group is the Stern-Brocot tree with signs!", confident that with my skillset it would be fairly straightforward for me to figure out what exactly that meant. Fifty days later, I started work in earnest.  In the meantime I skimmed Marcus Shell's recent master's thesis "Streaming Down the Stern-Brocot Tree". I found the word "lobe" to be evocative vocabulary, so I adopted it into my own thinking, but the thesis seemed to be asking the very questions I was planning to find an answer to.

As I started work in earnest, firstly, I chose the term SL(2,N) to refer to the matrices of determinant one that have natural (i.e. nonnegative integer) entries.  Then I found that every element of SL(2,Z) can be written in exactly two ways as a product of an element of Z_4, then an element of SL(2,N), then an element of Z_4 again, sort of a _vulgar conjugation_ of SL(2,N) by Z_4. Secondly, I found that every element of PSL(2,Z) can be uniquely written as a vulgar conjugation of SL(2,N) by Z_2. Thirdly, I found that every element of GL(2,Z) an be written in exactly four different ways as a vulgar conjugation of SL(2,N) and D_4.

Coming back around to the symmetry group of the square was weird, because I had not expected that, at all. Nor was I expecting to find something so poetically pleasing as the discovery that the treasure that I was seeking but not wholly expecting was so simply entwined with what I already had. I thought I had my "aha!" moment a week ago, and here I discover my sparring partner quite accidentally handed me the missing piece I didn't even know I needed to complete the then partially assembled jigsaw puzzle that was "Kevin Bacon and the Stern-Brocot Tree"!

A day or two later, I realized that I could have expected D_4 in the solution I was seeking:  after all, D_4 is precisely those 2x2 matrices with entries in {-1, 0, 1},  and determinant in {1, -1}.  Although linear algebra had long been firmly in my hotlist of mental associations with D_4, coming back from the other direction... not so much. Here finally was the "aha!" moment looking back inwards, reminding me that a heuristic blunder that I'm prone to making is underinvesting in efforts to make links in my memory palaces more bidirectional, and reminding me yet again that my appreciation of linear algebra can always be better.

This lead me to think back to my demonstration of D_4's action to Larry Moss, when as an aside I explained the weird thing I found with my D_4 calculator. It was actually meta-weird: when I first started drawing the D_4 calculator on paper for the first time, something about the principles I couldn't quite articulate but was committing to in order to develop the visual pun, gave me a strong sense that I would find an unexpected reward for my expense.  I was expecting the unexpected, and then I found it: after I finished, it didn't take me long to observe that by mentally moving the "window" on this book of algebra from the 12 o'clock position to the 3 o'clock position, the calculator works flawlessly, even though different physical glyphs are involved on the obverse side!  Try it!

I always love to see a couple of "weird", unexpected things come out of an idea, this was in fact part of the original connation of the word "collorary" in ancient Greek mathematics. In my mind, it's a good clue that you might be onto something important. These recurrent insights into linear algebra, and the surprise reappearance of an aggregate, was deeply pleasing. This time, understanding the modular group was far more than my meta-weird collorary, it felt like a total firestorm of unexpected insight, far grander than when I had first understood the Stern-Brocot tree.

Not long after this greater firestorm, I was going back through other mathematical memories, reviewing them in light of fresh insight. My thoughts returned to Elizabeth and Mark and other people at Case for the first time in many years. Because of this, late in the evening on December 15th, 2021, after it became clear that we would be saying goodbye to one of our much loved, elderly cat Lucy the next day, I learned Elizabeth had passed away on December 16th, 2020 after a short and unexpected illness. And I learned that Elizabeth and Mark had recently published "Linear Algebra", which motivated me to expand the scope of my literature review, which turned into this study guide.

Linear algebra is one of those subjects in mathematics that bring unexpected insight quite often. In retrospect, I believe that a significant part of my past and current philosophies of mathematics can be explained by a strong instinct to seek out combinations of ideas that are much more than the sum of their parts, and to delight in any strongly non-linear design gestalts that I can discern.

Perhaps this is part of the reason I have been slow to properly appreciate linear algebra, despite knowing a fair bit about it. This is most definitely a common phenomenon among professional mathematicians, even if the plausible causes in my case are not. By now I am well aware that I could dramatically level-up my mathematical skills by developing a habit of looking for linearity much earlier and much more aggressively. Twenty years have gone by since a serious review, and that's why I hope to use "Linear Algebra" by Meckes & Meckes as part of a process to relearn linear algebra yet again.

## A research program for Aggregate Theories of Concrete Mathematics

> The more ambitious plan may have a better chance of success.
>
> - George Pólya on the _Inventor's Paradox_, in "How to Solve It"

### The initial core of the program

Apply iterative deepening depth first searches to the following starting points:

1. Counting (up to 10 or less)
2. The Number Line (of the natural numbers).
3. Addition of small numbers (say, total not more than 5 or so)
4. The Stern-Brocot Tree (and the Euclidean Algorithm)
5. Pascal's Triangle
6. Symmetry Group of the Square

As soon as practical, mix in practices that exercise the inductive attitude, computer programming, problem solving, heuristics, self-awareness, self-control, and social skills.

Teachers need to keep in mind major milestones that should be achieved, including computer programming,, Boolean logic, binary numbers, types, Cartesian coordinates, geometric modelling, dimensional analysis, the arithmetic of fractions, binary search, depth-first search, breadth-first search, iterative deepening, radix-point arithmetic, limits of Stern-Brocot sequences, divergent sequences, counting combinatorially, matrix arithmetic, probability, statistics, inductive reasoning, deductive reasoning, recursion, syntax and parsing, and proof by induction. Teachers need to assist reaching simple milestones in these topics as early as is reasonable.

A first exposure to an idea or concept need not be a deep exposure: it only needs to be deep enough to establish a sturdy memory tripod or two, ideally by relating the concept to one or two other ideas in the curriculum. A secondary goal for an ideal lesson should be to drop some breadcrumbs and suggested readings that will hopefully create a mental reference in many students, and that hopefully a few students will someday follow up on.

Letting some period of time elapse before introducing the next big idea in a progression is a good thing.  Doing so will be an excuse to relearn the previous lesson.  It's okay if sometimes those periods of time are extended: for example, I expect the course of study outlined in Kevin Bacon and the Stern-Brocot tree to unfold over years for most children and younger teens, while they learn and practice plenty of other mathematical ideas and concepts too.  Spaced repetition is a proven memory enhancement heuristic for building long-term memories that are easily recalled.

### Robotics and The Third Little Induction

This essay started out by discussing inductive reasoning, in particular informal inductive reasoning via the inductive attitude.  Secondly I mentioned in passing that all-important deductive proof by induction, often first introduced in discrete math.   Robotics brings a third kind of induction: electrical induction.  I highly recommend early childhood exposure to simple electronics and robotics work, such as building computer-controlled LEDs, relays, actuators and motors via Arduino and Raspberry Pi types of devices.

We will focus on computer-controlled relays for a moment, because the common general-purpose relay's solenoid is an example of an inductive load that can result in damaged electronics projects if this is not taken into account. The relay's solenoid is a coil of wire that acts like an electromagnet: the magnet is turned on and attracts the relay's arm if there is electrical current flowing through the solenoid's coil. If there is no current flowing through the solenoid, then the magnet turns off, and a spring pushes the relay's arm away from the electromagnet.

A general-purpose input-output (GPIO) line from a CPU, microcontroller, or IO perhiperhal is pretty much never capable of driving a common relay; the solenoid is going to require more electrical power to actuate the arm than the GPIO line can safely deliver without risking damage to the CPU. The common solution is to use the GPIO signal to drive an NPN bipolar junction transistor that acts as a low-side switch for the solenoid.  This behaves like a very simple power amplifier to solve the first half of our problem: turning the solenoid on safely, thus actuating the relay's arm.

But the second half of our problem has another issue lurking: solenoids are examples of a reactive load, and we have to turn the relay off without damaging anything. When you first apply voltage to the solenoid, the magnetic field starts to turn on.  As the magnetic field grows stronger, it pushes against the electrons that are flowing through the coil.  This creates a reactive resistance that starts off strong and decays away as the magnetic field fully turns on. This reactive resistance is linked to the fact that inductive loads resist changes to the current flowing through them.

Similarly, the magnetic field stores a small amont of potential energy, and when you turn off the solenoid, the magnetic field starts collapsing.  This changing magnetic field keeps pushing the electrons in the coil along. This creates a reactive current that continues to flow for a short while even after the voltage potential goes away. This is an example of back-EMF, short for electromotive force. Left unchecked, back-EMF can create voltage spikes much higher than the voltage you energized the coil with, and those voltage spikes can damage or destroy equipment. Sometimes the failure might happen after one or two cycles, and sometimes it takes tens or hundreds or more cycles before the equipment stops working and it becomes apparent that there is a problem.

Handling back-EMF is a whole topic in and of itself. On the more sophisticated end of spectrum, all modern electric vehicles, some modern electric golf carts, and a few e-bikes implement regenerative breaking, using the abundance of back-EMF in this operating mode in order to charge the vehicle's batteries a little bit while breaking, thus extending range.

But we are dealing with small, common, general-purpose relays in our scenario. In this context, a common solution is to use a flyback diode to diffuse the kick of the back-EMF before it can build up into a damaging spike in voltage. A nice breadboard demonstration of a flyback diode in action is to use a light-emitting diode as the flyback diode of a relay, and have the relay's solenoid controlled by a push-button.  Properly done, the relay will actuate when you hold the button down, and the LED will flash when you release it.

Setting up a breadboard and demonstrating this effect, followed up by building a computer-controlled relay, is an excellent exercise that, with the right facilitation, could be successfully accomplished at a surprisingly early age.

There's far more that can be done along these lines, from amateur radio, 3D printing, playing with small robotic cars, robotic arms, CNC machines, etc. The material cost (both recurring and capital) of providing these sorts of activities, and doing so in a relatively hands-on way, is quite inexpensive relative to what has been possible in the past. We can afford to provide these interventions to everybody, and to encourage the development of the moral courage to make friends with rivals and to become better people. The main missing ingredients are human capital, payroll, and the will to make it happen.

### Details left to be worked out

What milestones should a college-prep K-12 curriculum starting from this point try to include?  This level of curriculum reorganization allows for surprising new pedagogical avenues, so deep re-examinations are very much warranted.  It's well worth looking at advanced books like Tristan Needham's Visual Differential Geometry and Forms in order to find clues about which ideas might be worth incorporating into the K-12 curriculum in order to prepare students to later study these books as effectively as possible.

For example, I'd love to hear more about Tristan Needham's use of ultimate equality in a first year calculus course.  Ultimate equality is the propositional statement that the limit of the ratio of two sequences is equal to one.  I would love for somebody to engineer a way to introduce and motivate ultimate equality, or at least introduce hints towards ultimate equality, in the K-12 curriculum. Automatic Differentiation is another strong candidate for this sort of treatment, which is an underappreciated, relatively recent technique detailed in "Software Design for Flexibility" by Chris Hanson and Gerald Jay Sussman.

Understanding the design philosophy of the Aggregate Theory is really appreciating the non-linear design gestalt behind the wisdom that is learning how to play the Six Degrees of the Square, Triangle, and Tree very well indeed.  This is a shockingly effective heuristic for discovering how to connect any particular idea to this new curriculum.

I mean, one of my goals for the design was to be able to trace out plausible paths, ideally short and simple paths, to teaching and learning as many different ideas as possible. For example, I very much want to see a particularly nice introduction to the Fourier transform in high school.

It's ok if the approach to the Fourier transform is primarily intuitive, informal, and applied; in fact that's all I personally have. I don't (yet?) have a deep theoretical understanding of the Fourier Transform.  Of course, I would very much like to see many hints towards this latter understanding worked into the informal, more applied introduction.  But that's definitely outside my wheelhouse, at least for the time being.

I am, however, supremely confident that such a plan can be created. As an obvious starting place, discussions of the Fourier transform can be naturally motivated by studies into music, sound, and amateur radio. In fact, I have rough ideas of how the aggregate theory connects to almost all of the mathematics that I have a minimal referential understanding of, i.e. anything more than just a name.  And of course, the much smaller subset of mathematics I am truly competent in, is nicely covered by the aggregate theory..

This larger category covers pretty much the entire core of a mainstream undergraduate mathematics curriculum, as well as some advanced undergraduate and early graduate-level topics that have been demonstrated to have great strategic value. But what if you don't even have a vague idea of how to incorporate an idea into your theory of mathematics?

You can always add that idea as a primary or secondary or tertiary starting poing for your personal theory of mathematics.  I suggest starting from the aggregate theory of concrete mathematics, and build on it and customize it.  Take any mathematical idea at all, and try to find answers about how it connects to the six degrees of your theory.  If you can find a connection (or two, or three, or...), great, you are starting to build your memory palace!

It's well worth the effort to aggressively combine, simplify, split, prune and compress the starting points of your personal aggregate theory.  Can one idea replace several others?  Of course, the ideas being removed from your starting points should still be remembered.  You aren't forgetting about them, you are just moving them to your memory palace.  They are part of your museum of mathematics, they just aren't a starting point for your theory of mathematics.

This is part of the reason why formal deductive logic is an explicit global recommendation of this study guide; I just couldn't quite find a connection I was satisfied with from the primary aggregates to deductive logic.[^deductive-logic-and-the-aggregate-theory] Another reason is that deductive logic (both formal and informal) is just too important to not explicitly recommend somewhere.

Pascal's Triangle leads quickly to the binomial coefficients, and these are directly relevant to first introductions to probability, statistics, and formal inductive logic. Although the Stern-Brocot tree and the symmetry group of the square are less directly relevant to a first introduction to probability and statistics, they are indisputably a very useful pedagogical device to introduce a little bit of linear algebra, which naturally feeds back into relatively accessible examples earlier in probability and statistics.

For example, Markovian processes can be modelled and simulated using matrix arithmetic. See Project Euler Problem #84,  which asks participants to write a program to calculate the most frequently visited squares in the board game of Monopoly.  This problem statement omits irrelevant rules, and simplifies the modelling of Chance, Community Chest, and Jail in ways unlikely to matter to the question being asked, in order to keep the resulting model small and simple.

The Haskell Road to Logic, Maths, and Programming, by Kees Doets and Jan van Eijck
  * This book is the closest approximation that I know of, to what I believe a discrete math class should aspire to be.
  * Many opinions on chapters 8 and 9, though my rewrite of those chapters would likely come out a bit longer
  * For example, I would probably discuss the Integer-Valued Polynomials
      * more abstract and more general than Pascal's Triangle.
      * more concrete and more specific than hypergeometric summations
      * practical pencil-and-paper method for finding closed-form solutions for discrete polynomial summations
      * good for high school contest mathematics
      * an induction schema: induction over IVPs
      * IVPs are well connected to combinatorics and linear algebra, with hints towards functional analysis
      * IVPs are an object specifically of interest in algebraic topology (But I don't understand why, yet.)
  * The binomal theorem used in the book precedes Sir Issac Newton.  Calling it "Newton's Binomial Theorem" without generalizing the binomial coefficients to the real numbers is definitely weird; I decidely do not like that linguistic precedent.  On the other hand, my rewrite would most definitely include at least a blurb about Newton's Binomal Theorem, and a mention of hypergeometric summation.
  * Chapter 10 is absolutely brilliant, and I'm sure my understanding of it could be deeper.
  * Chapter 10, Douglas McIlroy's "Music of Streams", and Project Euler demonstrates that a simplified, applied introduction to generating functions via combinatorics, formal power series, and lazy evaluation can be very approachable.
  * Personally, I would love to see an introduction to generating functions in high school. This book hints at an approach that seems promising.
  * See also "Discrete Mathematics with Ducks" for an attempt of comprehensive coverage of the ACM SIGCSE approved curriculum.
  * See "Concrete Mathematics", as a natural followup.

Structure and Interpretation of Computer Programs, by Harold Abelson and Gerald Jay Sussman
  * The Reasoned Schemer, by Daniel P Friedman
  * Essentials of Programming Languages, by Daniel P Friedman and Mitchell Wand
  * Software Design for Flexibility, by Chris Hanson and Gerald Jay Sussman

Order Theory and Lattices
  * Topic deserves to be more widely understood and appreciated.
  * In contemporary US culture, there seems to be a widespread assumption that all orders are total, and that the only alternative is that no comparisons are possible. This leads to unnecessary posturing, awkward conversations, and nonsensical cultural fixations.
  * A widespread appreciation for partial orders has the potential to transform the conversations we have with each other.
  * Note difference in lattices (geometry and linear algebra, e.g. modular group) and lattices (order theory)
  * Galois connections on partially ordered sets (posets) have a large number of applications:
     * Data Compression, Succinct Data Structures
     * Machine Learning, Formal Concept Analysis, Ontological Discovery
     * Programming language semantics
        * domain theory
        * abstract interpretation
     * Logic, Model Theory, Topoi
     * Combinatorics
     * Topology
  * Books are relatively few in number, and most are expensive, suggesting the topic deserves to be more widely appreciated even among mathematicians.
  * Classics include Garrett Birkhoff's "Lattice Theory" and Davey and Priestley's "Introduction to Lattices and Order, 2nd Ed."

Visual Group Theory by Nathan Carter
  * I too spent some time with Hungerford with Dr. Ta-Sun Wu.
  * Lovely effort to make abstract algebra more accessible
  * nicely thought out problem sets!
  * I believe I would have learned more abstract algebra more rapidly had this book been available
  * This book is very complementary to my own ideas along the same lines
  * If VGT is a introduction/adjunct to Fraleigh and Hungerford, I think the Aggregate Theory of Concrete Mathematics can readily produce an introduction/adjunct to Visual Group Theory.
  * Paolo Aluffi's "Algebra: Notes from the Underground" seems like a potentially interesting followup.
  * For a deeper look at quaternions, see "Geometry: Plane and Fancy", "Introduction to the Theory of Numbers", and some abstract algebra books.  Most introductory abstract algebra books only cover the finite quaterion group, though.

Neverending Fractions, An Introduction to Continued Fractions, by Jonathan Borwein, Alf van der Poorten, Jeffrey Shallit, and Wadim Zudilin.
   * Standard introduction to continued fractions, alongside an eclectic mix of less common applications.
   * I remember playing with Somos sequences via OEIS, but I never did anything very interesting with them.
   * See also Linas Vepstas's fascinating expository efforts to discuss this material in relatively accessible ways, often with an eye towards analysis and measure theory

An Introduction to the Theory of Numbers (6th Ed.) by
   * should do deeper review of this book
   * KB&SBT mentions that the converse of theorem 28 is also true, which isn't clearly mentioned in the book
   * theorem 29 is more general that what I had known to be true after writing KB&SBT

Geometry of Continued Fractions, by Oleg Karpenkov
   * This is quite an advanced look at topics closely related to the Stern-Brocot tree
   * Further suggestions in this vein include:
   * Algebra: Chapter 0, by Paolo Aluffi
   * Integral Matrices, by Morris Newman
   * Topics in Geometric Group Theory, by Pierre de la Harpe
   * Automorphic Forms and Even Unimodular Lattices, by Chenevier and Lannes

Proofs from THE BOOK

Game Theory
   * We need an excuse to play games in the math classroom
   * The goal should be to develop good, sometimes rigorous understandings of strategy
   * Need programming environments to be able to develop strategies and play-test them against each other tens of thousands of times.
   * opportunity to discuss/use
       * tradeoffs between pareto-optimal choices
       * probability
       * Markov chains
       * nimbers, combinatorial game theory
       * alpha-beta search
       * Monte Carlo Tree Search, etc.
   * seems like a good way to engineer excuses to play with SAT and SMT solvers and other kinds of model checkers, maybe even modal logic, etc.
   * "Theory of Games and Economic Behavior", by John von Neumann and Oskar Morgenstern
   * "Winning Ways for Your Mathematical Plays", by Elwyn R. Berlekamp, John H. Conway, and Richard K. Guy
   * "Chance, Strategy, and Choice", by Samuel Bruce Smith

# Navigation

[Part 4: Physics and Metaphones](./Part04_Physics_and_Metaphones.md#physics-and-metaphones)

[Part 5: an Invitation to the State of California](./Part05_an_Invitation_to_the_State_of_California.md#an-invitation-to-the-state-of-california)

[Author Bio](./Part05_an_Invitation_to_the_State_of_California.md#author-bio)

[Bibliography](./Bibliography.md)

[Part 1: Global Suggestions](./An_Aggregate_Theory_of_Concrete_Mathematics.md#tools-of-math-construction)

[Part 2: Deconstructing Bertrand Russell](./Part02_Deconstructing_Bertrand_Russell.md#deconstructing-bertrand-russell)

[Part 3: an Aggregate Theory of Concrete Mathematics](./Part03_Aggregate_Theory.md#suggestions-for-further-study)


[^graphicallinearalgebra]:
    I suggest reading the post [Makélélé and Linear Algebra](https://graphicallinearalgebra.net/2015/04/23/makelele-and-linear-algebra/), which states things quite nicely. See also "How Not to Be Wrong", by Jordan Ellenberg. I also really appreciated [Why string diagrams?](https://graphicallinearalgebra.net/2017/04/24/why-string-diagrams/), which I found to contain a nice acknowledgement of the difference between _pedagogical_ versus _motivating_ examples.

    For example, the Stern-Brocot tree is an excellent _pedagogical example_ for the study of coalegbra and coinduction, in the sense that if a student is interested in these topics, I wouldn't hesitate to recommend the Stern-Brocot tree, as it's a relatively simple and hopefully illuminating example for learning about coalgeba. Perhaps it provides enough intellectual texture to break syntactic illusions and more easily discover what makes coalgebra interesting, but at the very least I hope it provides a bit of gas to stimulate the imagination.

    I am far from certain that the Stern-Brocot tree is a _motivating example_ for the study of coalgebra, in the sense that if a student is specifically interested in the Stern-Brocot tree, I'm currently unlikely to suggest coalgebra for further study without another reason or two to make that specific recommendation. Of course, it would almost certainly be an interesting thing indeed, if somebody would make a convincing argument that the Stern-Brocot tree in fact motivates the study of coalgebra.

[^nandnor]: I also considered binary operators that were commutative, but not associative. I came up with such a binary operator inspired by "who wins rock-paper-scissors?", but more symmetric. On the other hand, I have yet to find a natural pedagogical motivation for such a thing. In the process of writing "Kevin Bacon and the Stern-Brocot Tree", I realized that NAND and NOR gates are commutative but not associative, which are easily motivated in the context of boolean algebra and digital logic design. See for example, "Computer Engineering for Babies" by Chase Roberts.

[^alternatives]: D_3, the symmetry group of the triangle, and Q_4, the quaternion group, are the only finite non-abelian groups that are less than or equal to D_4 in size. While these are both extremely interesting in their own right, neither seem to fit my criteria nearly as well. Similarly, the finite symmetric groups S_n of permutations are also very important, but it seems more concrete to use D_4 to introduce and motivate S_4 than vice-versa.

[^sbt-undergraduate-retrospective]: In retrospect, I quite sure multiple people at Case, including Dr. Singer and Dr. Zhang, encouraged me to understand continued fractions, but I never did quite catch on. On the other hand, the Stern-Brocot tree is such a fertile idea that I can also easily imagine suggestions that in retrospect suggest it's connection to the Euclidean Algorithm, when there was no such intention behind the suggestion.

[^barwiselakoff]:
    Which is funny, because in Barwise and Moss's 1991 article on "Hypersets", Jon Barwise starts out by analogizing a hyperset with the continued fraction of the golden ratio. Amazingly, Lakoff and Núñez's "Where Mathematics Comes From" is a direct reason why I made this connection at all. I didn't review this book until I was deep into writing this study guide, and the bit about hypersets and continued fractions was the first page I accidentally turned to. Glancing at that, I immediately looked at the bibiliography and citations, followed the reference back, and reviewed Barwise and Moss's article for the first time.

    It's really satisfying when ideas come back around full circle.  When I was struggling to get started with "Kevin Bacon and the Stern-Brocot tree", it wasn't until I really started thinking about George Lakoff's concepts of framing that I could find my voice.  I'm only referentially familiar with Lakoff's work on this matter, perhaps someday I'll get around to actually reading "Don't Think of an Elephant!"

[^deductive-logic-and-the-aggregate-theory]:
    From a certain very strict notion of relevance that I have often worked from while writing this essay but can't quite explain, the six degrees of the primary aggregates (i.e. the tree, the triangle, and the square) doesn't seem to connect to formal logic until you get to graduate-level model theory and algebraic semantics.

    Even then, the connections still seem secondary and indirect, using the aggregates as pedagogical devices to introduce algebra, partial orders, and topology. I'm still not aware that the aggregates are directly relevant to a goal of learning graduate-level model theory, though I am certainly interested in having my mind changed on this topic.

    But from the point of view of motivating deductive logic in a K-12 curriculum redesign, this observation seems to be of no immediate interest. I certainly believe the primary aggregates help set an engaging stage for learning about deductive logic.  In the larger theory, the secondary aggregates are heuristics, computer programming, and problem solving. The Six Degrees of these Secondary Aggregates provides plenty of natural motivation to study deductive logic, at varying points along the formal/informal spectrum.

    I do sincerely hope that in a hundred years time, algebra, partial orders, and topology will be somewhat common and not considered nearly so highminded. These conditions should help make model theory far more approachable, if one is so inclined to study it. However, it seems highly implausible to me that an approach through graduate-level model theory will someday directly compete with the Six Degrees of the Secondary Aggregates. Computer programming, problem solving, and heuristics seem to provide far more natural and elementary routes into deductive logic.