# Tools of Math Construction: An Aggregate Theory of Concrete Mathematics
# by Leon P Smith, Iterative Systems

In celebration of Rational Approximation Day 02022-07-22, and in the name of Reason and a Reënlightenment, I offer an apology for the Indiana Pi Bill, and an Apology for Science, Faith, Reason, and Humanity.  This study guide is a companion to [_Kevin Bacon and the Stern Brocot Tree: a Sermon on Rational Approximation_](../T001_Kevin_Bacon_and_the_Stern-Brocot_Tree/a_Sermon_on_Rational_Approximation.md)

[![Philosophy News Network: is Philosophy Useless?](external-assets/static.existentialcomics.com/comics/PhilosophyNewsNetworkisPhilosophyUseless1.png)](https://existentialcomics.com/comic/365)
[![Philosophy News Network: is Philosophy Useless?](external-assets/static.existentialcomics.com/comics/PhilosophyNewsNetworkisPhilosophyUseless2.png)](https://existentialcomics.com/comic/365)

If you only ever read a single suggestion, I would ask that you read "Weapons of Math Destruction", as it is directly relevant to the state of the world today and the many contemporary challenges we face. I suspect a great many people should probably read "The Scout Mindset" first, as preparation.

My global suggestions consist of ten primary recommendations loosely divided into three major themes: inductive reasoning and self-awareness, ethics and morality, and the philosophy of math and science. These suggestions are "global" in the sense that I would recommend them to most people, with relatively few conditions or qualifications.

Later, I [deconstruct Bertrand Russell](./Part02_Deconstructing_Bertrand_Russell.md) and endorse the Weak Paraconsistent Conjecture in memory of Jon Michael Dunn.

Then I share an intellectual history of my thinking on [an Aggregate Theory of Concrete Mathematics](./Part03_Aggregate_Theory.md). These are stories of creative interactions between myself and others that contributed to my learning and occasional re-discovery of some well-known yet widely underappreciated results. These results deserve a much broader audience. This intellectual history doubles as a tribute to Linear Algebra and the memory of Elizabeth Meckes.

In [Physics and Metaphones](./Part04_Physics_and_Metaphones.md), I share a modern, popularized account of Claude Shannon's Theory of Communication, a modern take on Ludwig Wittgenstein's semantics of language, and engineering considerations for practical implementations. This explores issues of noise, authentication, queueing, protocol, and consensus, and how they relate to things such as amateur radio, emergency management, cryptography, and blockchain. It attempts to provide a holistic summary of several relatively conventional takes on the modern philosophies of the design of communications systems. I deconstruct APRS, the Automatic Packet Reporting System, suggesting that it should inspire a next-generation amateur radio protocol intended towards disaster relief, as a tribute to the memory of the silent key Bob Bruninga, WB4APR.

Finally, in honor of my former classmate and dear friend Yuri Goldfeld, I extend an [invitation to the State of California](./Part05_California_Math_Curriculum_02022.md) to strengthen the foundation of the elementary mathematical curriculum with the Six Degrees of the Square, the Triangle, and the Tree, constructive symmetry, computer programming, rational approximation, robotics, and induction.

This invitation extends to you personally, as well as the United States of America and all of human kind. Everybody deserves to be included in and benefit from math curriculum reform.

To celebrate, I suggest [cutting a pie into sevenths, and sharing it with a circle of six other friends](./Part05_California_Math_Curriculum_02022.md#sharing-pie-with-a-circle-of-friends), both new and old. May you have a blessed Rational Approximation Week, and a wonderful Rational Approximation Day.

[![Philosophy News Network: Philosophy Solved](external-assets/static.existentialcomics.com/comics/PNNphilosophySolved1.png)](https://existentialcomics.com/comic/191)
[![Philosophy News Network: Philosophy Solved](external-assets/static.existentialcomics.com/comics/PNNphilosophySolved2.png)](https://existentialcomics.com/comic/191)

> Every difficult problem has a solution that is simple, neat, and wrong.
>
> paraphrased from H.L. Mencken

## Global Suggestions

* Self-aware, Inductive Reasoning:

    1. The Scout Mindset: Why Some People See Things Clearly and Others Don't, by Julia Galef
    2. Benjamin Franklin: A Film by Ken Burns
    3. The Knowledge Illusion: Why We Never Think Alone, by Steven Sloman and Philip Fernbach
    4. The Book of Why: The New Science of Cause and Effect, by Judea Pearl and Dana Mackenzie

* Ethics and Moral Philosophy:

    5. The Ethics of Belief, by William Kingdon Clifford
    6. Weapons of Math Destruction: How Big Data Increases Inequality and Threatens Democracy, by Cathy O'Neil
    7. When Time Is Short: Finding Our Way in the Anthropocene, by Timothy Beal

* Philosophy of Math (and Science):

    8. Proofs and Refutations: The Logic of Mathematical Discovery, by Imre Lakatos
    9. Language, Proof and Logic (2nd Ed.), by Dave Barker-Plummer, Jon Barwise, and John Etchemendy
    10. Statistical Rethinking: A Bayesian Course with Examples in R and Stan (2nd Ed.), by Richard McElreath

Our contemporary culture likes to talk about, use, misuse and abuse math and science a lot, but what are these things, really?  Where does science come from?  What makes science "true"? Does mathematics provide "absolute" truth? What is "truth", anyway?  What are the differences between math and science, and how are they related? What are the material conditions in which math and science are conducted? What responsibilities do we have regarding what we believe to be true?

Every one of these questions is important, and, if we are being honest, every one of these questions is difficult, some moreso than others. At best, simple answers to these questions provide only crude approximations of reality, and at worst are wrong, misleading, and/or harmful. A key goal of my global suggestions is to provide useful answers to the parts of these questions that are relatively well-understood. Another key goal is to introduce schools of thought that have been useful in understanding and approaching the difficulties that these questions pose.

For an invaluable overview of philosophy, I highly recommend "The Great Conversation: A Historical Introduction to Philosophy" by Norman Melchert and David R. Morrow. It is an excellent reference book with an emphasis on Western perspectives.  Steven Pinker's "Rationality: What It Is, Why It Seems Scarce, and Why It Matters" has many significant overlaps with this study guide and its many reading recommendations, and is itself well worth reading.

[![Wittgenstein Revises His Thesis](external-assets/static.existentialcomics.com/comics/WittgensteinRevisesThesis.png)](https://www.existentialcomics.com/comic/292)

I didn't draw these comics, they are from Existential Comics.  The author of these comics often provide a useful summary and explanation of the comic, as is done in [Wittgenstein Revises His Thesis](https://www.existentialcomics.com/comic/292) above. Check it out!

## Self-aware, Inductive Reasoning

[![Star Trek: but instead of normal, it's with philosophers](external-assets/static.existentialcomics.com/comics/starTrek1.jpg)](https://existentialcomics.com/comic/92)
[![Star Trek: but instead of normal, it's with philosophers](external-assets/static.existentialcomics.com/comics/starTrek2.jpg)](https://existentialcomics.com/comic/92)

The goal of my first theme is to introduce what George Pólya calls the _inductive attitude_:

> In our personal life we often cling to illusions. That is, we do not dare to examine certain beliefs which could be easily contradicted by experience, because we are afraid of upsetting our emotional balance. There may be circumstances in which it is not unwise to cling to illusions, but in science we need a very different attitude, the _inductive attitude_. This attitude aims at adapting our beliefs to our experience as efficiently as possible. It requires a certain preference for what is matter of fact. It requires a ready ascent from observations to generalizations, and a ready descent from the highest generalizations to the most concrete observations. It requires saying "maybe" and "perhaps" in thousand different shades. It requires many other things, especially the following three.
>
> First, we should be ready to revise any one of our beliefs.
>
> Second, we should change a belief when there is a compelling reason to change it.
>
> Third, we should not change a belief wantonly, without some good reason.
>
> These points sound pretty trivial. Yet one needs rather unusual qualities to live up to them.
>
> The first point needs "intellectual courage." You need courage to revise your beliefs. Galileo, challenging the prejudice of his contemporaries and the authority of Aristotle, is a great example of intellectual courage.
>
> The second point needs "intellectual honesty."  To stick to my conjecture that has been clearly contradicted by experience just because it is _my_ conjecture would be dishonest.
>
> The third point needs "wise restraint." To change a belief without serious examination, just for the sake of fashion, for example, would be foolish. Yet we have neither the time nor the strength to examine seriously all of our beliefs. Therefore it is wise to reserve the day's work, our questions, and our active doubts for such beliefs we can reasonably expect to amend. "Do not believe anything, but question only what is worth questioning."
>
> Intellectual courage, intellectual honesty, and wise restraint are the moral qualities of the scientist.
>
> - G. Pólya, "Mathematics and Plausible Reasoning, Vol I: Induction and Analogy in Mathematics", Chapter 1, Section 4. See also "On Rearing Scholars" by Imre Lakatos, as translated by Ninon Leader as Appendix A of "For and Against Method" by Imre Lakatos and Paul Feyerabend, edited by Matteo Moterrelini.

Properly respecting uncertainty and doubt, by learning how to hold onto uncertainty without unreasonably clinging to doubt, is a fundamental ingredient to making inductive reasoning work well. For a contemporary, easy to read, and compelling introduction to the _inductive attitude_, I highly recommend "The Scout Mindset" by Julia Galef. The author provides a brief video overview of her thesis in [Why you think you're right - even if you're wrong](https://www.ted.com/talks/julia_galef_why_you_think_you_re_right_even_if_you_re_wrong) TED talk.

From watching "Benjamin Franklin, A Film by Ken Burns", I believe that this founding father was frequently a master practitioner of the scout mindset throughout his life. Of course there are cases, even in this documentary, where Benjamin Franklin didn't live up to this ethos very well. It's important to remember that the inductive attitude is a process, not a destination. Past performance does not determine future outcomes. The Scout Mindset is not a label to be acquired or trophy to be won. Instead, the scout mindset is an often deteriorating state of being that can always be improved upon and can only be re-earned. The scout mindset has very little to with where you currently are at, and a lot to do with your attitude about where to go next. Compare this to "Don't Label Me" by Irshad Manji, and NBC's philosophical comedy "The Good Place".

George Pólya observed that we "have neither the time nor the strength" to carefully examine everything we believe. In "The Knowledge Illusion", Steven Sloman and Philip Fernbach expand on this idea in at least two ways. Firstly, the authors draw a distinction between the things of which we have direct, immediate knowledge, and the things of which we have indirect, referential knowledge. Secondly, they argue that people have a cognitive bias to believe that they have direct knowledge of a topic in cases where their knowledge is in fact referential. Kevin deLaplante provides a very nice introduction and summary of [The Knowledge Illusion](https://www.youtube.com/watch?v=LC6O_2vDDwc) on his YouTube channel.

I believe it likely that we, as a society, stand to all substantially benefit by being more honest about referential knowledge. Making that a reality would seem to involve at least three ingredients. Firstly, large numbers of individuals need to make fewer mistakes of confusing their own referential knowledge for direct knowledge. Secondly, we need commonly understood linguistic cues that succinctly communicate whether the knowledge you claim to have is referential or direct. Thirdly, we all need to live in a society of peers with a keener understanding of both the value and the limitations that referential knowledge represents. After all, if we as a society routinely dismiss the referential knowledge of others out of hand, then future conversations are less likely to be had, and the linguistic cues are less likely to be used. All three steps promote a common theme: raising the self-awareness of all the individuals of a society.

Note that "direct knowledge" versus "referential knowledge" is my own terminology, not used by the authors. My thinking is by analogy to the theory of computer programming languages. For example, in some programming languages like C or Pascal, arguments to a procedure may be passed directly, or by reference. This particular distinction becomes semantically meaningless in purely functional programming such as Haskell, yet there are other analogous notions of "direct, immediate" versus "indirect, referential" that are relevant. Extending the analogy, "dereferencing" would be taking referential knowledge and turning it into direct knowledge, by the process of learning it for yourself.

"The Book of Why: The New Science of Cause and Effect" by Judea Pearl and Dana MacKenzie is written for the general public as an introduction to causal modelling via dot-and-arrow diagrams. It introduces The Ladder of Causality as a metaphor for the fundamental capabilities of observational statistics, causal inference, and counterfactual reasoning. Classical observational statistics does not intervene and thus cannot definitively answer questions of causality, so it forms the lowest rung of the ladder.

The tools of causal inference can be used to turn hypothetical models of relevant causes and effects into _estimands_, if possible, or say that no such estimand exists. Estimands are like statistical ovens that bake empirical data into estimates. It is impossible to definitively test a hypothetical causal model from observation alone.  For this, interventions are required in order to go one rung up on the Ladder of Causality. Yet formal causal models are the price to ascend another rung of the ladder, and in return enable repeatable counterfactual reasoning.

A conterfactual question is a "what if" question.  Formal counterfactual reasoning can be used to study the plausibility of the many different possible answers to such a question, all at the same time.  This uses a process that is repeatable, understandable, and can produce formal justifications for the answers that the model can represent.

Some level of awareness, either consciously, unconciously, by design, and/or by evolution, seems to be an essential ingredient in inductive and counterfactual reasoning. Self-awareness seems to be especially fundamental to making informal inductive reasoning work well in humans. Daniel Kahneman's "Thinking, Fast and Slow" reflects on a number of cognitive biases we all exhibit to varying degrees. Kahneman, Sibony, and Susstein's "Noise: A Flaw in Human Judgement" delves deeper into the cognitive mistakes humans naturally make and that groups sometimes amplify.

See also "Not Born Yesterday" by Hugo Mercier, which reflects upon the nature of persuasion, skepticism, and belief in individuals and societies. Douglas Hofstadter's "Gödel, Escher, Bach: a Eternal Golden Braid" is in part a speculative thesis on how human self-awareness might arise from strange loops, and in part an informal introduction to metamathematics and the art of self-reference.

[![Gottfried Leibniz and the Quest for the Holy Grail](external-assets/static.existentialcomics.com/comics/montyPython1.png)](https://existentialcomics.com/comic/108)
[![Gottfried Leibniz and the Quest for the Holy Grail](external-assets/static.existentialcomics.com/comics/montyPython2.png)](https://existentialcomics.com/comic/108)
[![Gottfried Leibniz and the Quest for the Holy Grail](external-assets/static.existentialcomics.com/comics/montyPython3.png)](https://existentialcomics.com/comic/108)

I've read translations of Leibniz's Monadology a couple of times, including when attending lectures of Larry Moss's. I don't know how the Monadology relates to those lectures, except by the shallowest of puns, or a perspective that includes metaphysical discussion the of lectures and its participants themselves (which might or might not include  the content of said lecture).

The Monadology is pretty short, but it is decidedly not easy reading. I've yet to understand most of it. Existential Comics provides their own original summary for this comic on their site.  This summary gave me a reason to reread the Monadology again. Check it out!

## Ethics and Moral Philosophy

[![An Ethical Dilemma Finally Resolved](external-assets/static.existentialcomics.com/comics/ethicalDilemmaResolved1.png)](https://existentialcomics.com/comic/258)
[![An Ethical Dilemma Finally Resolved](external-assets/static.existentialcomics.com/comics/ethicalDilemmaResolved2.png)](https://existentialcomics.com/comic/258)

This would be an example of a just act. See also ["What I Think About Atlas Shrugged" by John Scalzi](https://whatever.scalzi.com/2010/10/01/what-i-think-about-atlas-shrugged/), and "The Common Good" by Robert Reich.

[![Philosophy News Network: Strike](external-assets/static.existentialcomics.com/comics/PNNstrike1.png)](https://existentialcomics.com/comic/199)
[![Philosophy News Network: Strike](external-assets/static.existentialcomics.com/comics/PNNstrike2.png)](https://existentialcomics.com/comic/199)

John Rawls is known for "A Theory of Justice". Lawrence Krauss is known for "The Physics of Star Trek". Simone de Beauvoir is known for "All Men Are Mortal".  Hannah Arendt is known for "The Human Condition".

My second theme is ethics and moral philosophy, of the kinds most immediately relevant to the difficulties we currently face. Philosophy, science, and mathematics are tools of criticism and analysis. Although these tools are frequently capable of informing what we believe and how we behave in valuable ways, they are capable of compelling neither belief nor action. At the same time, what we believe impacts how we act, and how we act impacts the real world in tangible ways, thus creating _epistemic responsibility_: our moral responsibilities about the things we believe to be true.

William Kingdon Clifford famously wrote about epistemic responsibility in his classic short essay "The Ethics of Belief". It is best known for fable about ship's owner being recklessly optimistic about the seaworthiness of his vessel. I am very much convinced by Clifford's fable that epistemic responsibility exists,  even if I remain unconvinced by Clifford's attempt to extrapolate a more general theory of epistemic responsibility from his fable. For a discussion of the meaning of the word "reckless", and an introduction to the concept of _mens rea_ in general, I recommend [The Illustrated Guide to Law, by Nathan Burney](https://lawcomic.net). I found parts of Clifford's essay quite difficult to read, so I highly recommend [a short video on epistemic responsibility from Crash Course Philosophy](https://www.youtube.com/watch?v=AYkhlXronNk), which highlights William James' similarly important short essay "The Will to Believe" as the classic counterpoint to Clifford.

In terms of our moral, ethical, and epistemic responsibilities, the information technology sector is currently an disaster area to an apocalyptic degree. I very much hope that you do read Cathy O'Neil's "Weapons of Math Destruction". Further assessments can be found in "Algorithms of Oppression" by Safiya Umoja Noble, "Automating Inequality" by Virginia Eubanks, and "The Loop" by Jacob Ward. Significant social problems arising from the misuse of information technology were anticipated in the final chapter of the 1999 book "The Limits of Software" by Robert Britcher.

This phenomenon of highly problematic, suspect uses of "math", "science" and "reason" is not new:  see "The Mismeasure of Man" by Stephen Jay Gould for examples that predate modern information technology, such as phrenology. In fact, much of the earliest work on inductive logic, correlation, and statistics by Charles Sanders Peirce, Francis Galton, Karl Pearson, Ronald A Fisher and others was in fact motivated at least in part by trying to provide a justification for slavery, social Darwinism, class inequality, eugenics, and/or scientific racism.

While these motivations should rightly be recognized as moral refutations produced by our very human history, these delusions also produced geniune insight as a byproduct.  It would also be a mistake to dismiss that insight. However, please recognize that this is not a "Get Out of Jail free" card. Even today, issues that rhyme with these moral refutations continue to echo and to be recreated afresh under different guises. We very much still do need to address issues of how to use statistical ovens appropriately and how to interpret their estimates wisely.

Rounding out a crash-course in the moral dimensions of our current situation, I highly recommend Vaclav Smil's book "How the World Really Works", as well as Tom Murphy's blog "Do The Math" and his textbook "Energy and Human Ambitions on a Finite Planet: Assessing and Adapting to Planetary Limits". An evaluation of the thermodynamic bases of the economies of ancient cultures can be found in a number of Jared Diamond's books, including "Guns, Germs and Steel" and "Collapse". I admire the IPCC and the Long Now Foundation, and the work of Stewart Brand, James Hansen, and Michael Mann among many others.

I cannot imagine a more profound human tragedy than contemporary Christian eschatological fantasies enmeshed with the delusions of today's economic orthodoxy becoming a self-fullfilling prophecy. It would be a profound failure of humanity's moral imagination if we never even seriously attempted to address these issues. Unfortunately, this scenario is an objectively live option in the real world today. I highly recommend Timothy Beal's "When Time Is Short: Finding Our Way in the Anthropocene", as an attempt to answer the question why we don't look up. We as human societies also need to quickly figure out how to break out of a self-destructive fixation on GDP growth.  Elinor Ostrom's "Governing the Commons" and Kate Raworth's "Doughnut Economics" seems like promising starts.

On the topic of doughnuts, I suggest meditating on the Talmudic parable of The Oven of Akhnai, and "Sifting Through the Embers", a retelling of the fable of the Sibylline books found in Douglas Adams and Mark Carwardine's "Last Chance To See".  On the topic of meditations, I can't but help of thinking of Chidi's response to Simone's behavior in "The Good Place", and Yonatan Zunger's thoughtful essay "[Tolerance is not a Moral Precept](https://extranewsfeed.com/tolerance-is-not-a-moral-precept-1af7007d6376)".

> Chidi: No offense, but solipsism, as a philosophy, is pretty juvenile, especially for a person with multiple advanced degrees. And it's also impossible to refute, because everything you see is confirmed by your belief. However... [Chidi sticks his finger in Simone's frozen yogurt]
>
> Simone: Dude!
>
> Chidi: What? If none of this is real, then it really shouldn't matter, right? In fact... [Chidi boops her on the nose with his yogurty finger]
>
> Simone: Dude!
>
> Chidi: What? It's not real. None of this matters. Leave that on your nose for the rest of time.
>
> Simone: Fine. Point sort of taken.
>
> Chidi: You know, in a larger sense, if you go around acting like no one else matters, then you end up doing things like knocking over cakes, and pushing people into pools and just generally acting like a jerk. Why not treat them better, just in case they're real? I mean, what do you have to lose by treating people with kindness and respect?
>
> Simone: Okay. Keep talking, probably-fake but-maybe-real philosopher man.

[![The Philosophy Force Five vs the Scientismists](external-assets/static.existentialcomics.com/comics/philosophyForceFive1.png)](https://existentialcomics.com/comic/190)
[![The Philosophy Force Five vs the Scientismists](external-assets/static.existentialcomics.com/comics/philosophyForceFive2.png)](https://existentialcomics.com/comic/190)
[![The Philosophy Force Five vs the Scientismists](external-assets/static.existentialcomics.com/comics/philosophyForceFive3.png)](https://existentialcomics.com/comic/190)

I agree with the original summary provided by Existential Comics: in ways relevant to this essay, Neil deGrasse Tyson certainly seems ontologically distinct from the rest of the men depicted in this comic. I very much look forward to reading "Starry Messenger: Cosmic Perspectives on Civilization".

Gertrude Elizabeth Margaret (G.E.M.) Anscombe is well known as a moral philosopher in the analytic tradition, and for being a student, close friend, and translator of Ludwig Wittgenstein. She is strongly associated in my mind with "Anscombe's Paradox": the observation that if at least 5 electors vote on least 3 proposals passed by simple majority, and you consider the set of electors who voted against a majority of the proposals that passed, then that set might constitute a majority of the electors. It's not hard to synthesize a hypothetical example: it's essentially the same as "packing and cracking" in gerrymandering. Try it!

Elizabeth Anscombe pointed out this paradox, and demonstrated that if you try to use a supermajority rule to eliminate any possibility of this ever occurring, then a 3/4 supermajority is both a necessary and sufficient threshold. Any threshold less than 75% could theoretically allow this paradox to occur in some cases, though it certainly won't occur in all cases: with enough electors voting in increasingly specific ways, this outcome is an _a posteri_ empirical possibility, however unlikely. Whereas a 75% threshold would rule out any possibility of this outcome _a priori_, with the sole empirical assumption being that the rules are ultimately respected. We should realize by now that this is not always a safe assumption.

On the topic of practical social choice theory, in particular I support approval voting for single-winner elections and proportional representation for multi-winner legislature races.  I enthusiastically endorse the Center for Election Science, as well as "Gaming the Vote" by William Poundstone.  Among others I particularly admire the work of Birch Bayh, Rob Richie, John Anderson, Ka-Ping Yee, Brian Olson, Warren Smith, Aaron Hamlin, Jameson Quinn, J. Alex Halderman, Kenneth Arrow, Amarya Sen, and Elinor Ostrom.

## The Philosophy of Math (and Science)

[![Pride and Prejudice and Logical Positivism](external-assets/static.existentialcomics.com/comics/PrideandPrejudiceandLogicalPositivism1.png)](https://existentialcomics.com/comic/413)
[![Pride and Prejudice and Logical Positivism](external-assets/static.existentialcomics.com/comics/PrideandPrejudiceandLogicalPositivism2.png)](https://existentialcomics.com/comic/413)

"Proofs and Refutations: The Logic of Mathematical Discovery" by Imre Lakatos is an unusual book, not least because it explicitly argues in favor of informal mathematics. One of Judea Pearl's theses in "The Book of Why" is that discussing and formalizing causal inference has been so difficult, even controversial, precisely because we are naturally pretty good at it. By analogy, I suspect that discussing[^formalizinginformalmath] the philosophy of informal mathematics is in a similar situation. By constrast, classical statistics, deductive logic, and algebra come far less naturally to the human mind, which in some ways makes it easier to appreciate why they are important and interesting ideas to hold on to.

I am currently unaware of any single book that I feel could have had a greater positive impact on my mathematical education, than if had I read "Proofs and Refutations" while I was taking geometry my sophomore year of high school. I do believe this book could have dramatically improved the results of my math education along multiple axes. There certainly are many introductions to the Euler characteristic well worth recommending on their own terms, including David Richeson's "Euler's Gem", David Singer's "Geometry: Plane and Fancy", Tristan Needham's "Visual Differential Geometry and Forms", Aigner and Ziegler's "Proofs from THE BOOK", and sarah-marie belcastro's "Discrete Mathematics with Ducks". However, nothing I know of has the philosophical content of Lakatos' classic, delivered with humor and great historical depth.

Lakatos's philosophy of informal reasoning revolves around a sophisticated understanding of Pólya's inductive attitude and Popperian fallibilism as applied to mathematics. In fact, it starts where Pólya's "Mathematics and Plausible Reasoning" left off in its coverage of the Euler characteristic, and presents the history of this idea as a rational reconstruction of a boisterous class of students, with the "teacher" being a metaphor for the theorem itself and a narrative device to occasionally inject Lakatos's philosophy. It's title is an homage to both "Conjectures and Refutations" and "The Logic of Scientific Discovery" by Karl Popper. All of these books are well worth reading in their totality, but the preface to "Proofs and Refutations" is well worth reading sooner than later.

In fact, I was provided a very important lesson about the limitations of formal mathematics, when I was carefully evaluating Warren Smith's claims about Arrow's Theorem the first time I happened across them.  The lesson I took from my proof analysis is that Warren Smith is correct, and that his proof analysis helped highlight a very subtle pitfall of formal methods I had only been vaguely aware of, and that is the problem of attaching informal interpretations to our formal proof artifacts in correct and reasonable ways.   I call this the _Pitfall of Interpretation_.

These informal interpretations can be subtly incorrect in ways that can be infuriatingly difficult to detect. Informal reasoning can be done well or it can be done poorly, but to some degree or another, informal reasoning is _inescapable_. So an aspiring mathematician might as well embrace the situation and learn to do it well.

The good news is, with some basic social skills, a wise teacher or two, and few good role models, learning informal mathematics really isn't really that hard for most people most of the time.  I believe this fact explains why, most of the time, mathematicians can get away with pretending that we don't ever do informal mathematics.  I believe it explains why, most of the time, our pretensions seem to have little consequence. The consequences of these pretensions are much more subtle, and can be supremely difficult to disentangle from other causes when breakdowns do occur. This makes it very difficult to fully diagnose and easy to even outright misdiagnose the root causes of such a breakdown.

What I am saying should not to be misconstrued. To clarify, learning about a new-to-you mathematical idea in an informal way can be difficult, and is often very much so!  Rather, I am saying that learning the practice of informal mathematics is not so difficult _most_ of the time, because we do informal mathematics instinctively. In general, I recommend trying to always be open to learning how to improve your informal reasoning. The goal of informal reasoning is to become less wrong, and the very heart of informal reasoning is the _inductive attitude_.

However, inductive reasoning alone isn't nearly enough, especially not informal inductive reasoning such as the _inductive attitude_. Inductive reasoning must be formalized in order to truly come into its own. Formal inductive reasoning requires understandings of probability, statistics, and causal inference.  Formal inductive reasoning often requires careful experimental design that intervenes in the world in some way, and observes the results of that intervention.

Before we can reasonably do all of this, we need deductive reasoning, which gives us the tools to preserve truth, to justify truth, and to reliably reproduce truth.  Humanity's first introduction to deductive reasoning came to us via Euclidean geometry.  Here informal deductive logic proved very useful despite the fact that, by modern standards, the explication of deductive logic wasn't entirely clear and complete. As a result mathematicians were prone to making subtle deductive errors, falling short of modern standards of formality and rigor.

Yet at the same time, informal deductive reasoning was useful enough that the results were truly revolutionary, and maybe a little _too_ revolutionary in some ways. Among Western philosophers, Euclidean geometry became the received wisdom for more than two thousand years, before we took some Arabic and Semitic influences and Galileo started to push beyond Euclidean geometry with early investigations into the continuum and Calculus circa 1600.

It wasn't until 1830s or so until non-Euclidean geometry was commonly recognized as a logical possibility by well-informed mathematicians.  Work by Boole, Frege, Whitehead, Russell, and others from 1848-1917 that brought formal deductive reasoning up to modern standards of clarity and rigor.  This facilitated a revolution in metamathematics, computation, and algorithms by Gödel, Church, and Turing, among many other crucially important contributors.

And yet, the facade of mathematical dogmatism has stayed quite intact to this very day.  I believe it's possible, perhaps even plausible, that automated deductive theorem proving could enable and motivate a new golden era of informal mathematics.  Why, you might ask?

To borrow a turn of phrase, "The bottleneck is dead, long live the bottleneck!" is a simple summary why. If you can be quite confident that there does not exist a subtle but crucial mistake buried deeply in a formal proof, then you have more time and mental resources with which to contemplate mistakes in the informal interpretations and perceived practical real-world implications of that proof.  Very good mathematicians make mistakes on this count.

Also, because it seems likely that we could eventually find ourselves creating formal deductive proof artifacts for theorems far more complicated and ornate than what we've contemplated so far, it seems plausible that would induce demand for improving skills in informal mathmatics.

Of course, I am not suggesting that every proof must be formal, let alone sufficiently formal that a proof assistant can understand it! Good informal proofs are still interesting! Nor am I suggesting that every mathematician should be using a proof assistant. But I am suggesting that everybody should be familiar with deductive reasoning.

However, the modern world has already provided alternative options for learning deductive reasoning outside of geometry. I believe those options will be preferred by many students. Computer programming, logic puzzles, discrete math, and model theory are just a few of the better established alternatives. I am confident many more alternatives can be found and developed, especially in terms of the auxiliary topics used to motivate and discuss deductive logic. Indeed, I hope people do put the effort into finding and developing these paths, so that they may help serve better the goal of getting everybody acquainted with the basics of logical deduction.

[![Philosophy Network News: Derrida Arrested!](external-assets/static.existentialcomics.com/comics/PNNderrida1.png)](https://existentialcomics.com/comic/185)

[![Philosophy Network News: Derrida Arrested!](external-assets/static.existentialcomics.com/comics/PNNderrida2.png)](https://existentialcomics.com/comic/185)

"Language, Proof and Logic" is an introduction to formal deductive logic and model theory, and seems well suited for self study via computer-based exercises and online lectures. From the introduction, the sections "The special role of logic in rational inquiry", "Why learn an artificial language?", and "Consequence and proof" are particularly well worth reading sooner than later.

The title invokes "Language, Truth, and Logic" by A.J. Ayer, which was a popular English-language introduction to the logical positivism of Rudolph Carnap and the Vienna Circle. Bertrand Russell, Ludwig Wittgenstein, G.E.M. Anscombe, and Willard Van Orman Quine are other high-profile analytical philosophers whom appear in the Existential Comics I reference in this document. Logical positivism was an early form of analytical philosophy, which has grown into a workhorse of science, math, and computer engineering.

"Statistical Rethinking" by Richard McIlreath provides a modern introduction to statistics. The first chapter, "Statistical Golems" introduces the parable of the Golem of Prague as a metaphor for what this essay has been calling _statistical ovens_, or more properly _estimands_. The second chapter, "Small Worlds and Large Worlds", reflects on the difference between the small world of a mathematical model, which should ideally exhibit reproducable reasoning, and the large world of empirical reality, which does not, and indeed cannot.

Both chapters explicate serious deficiences with the philosophy of science as currently practiced today. They are available to download free of charge from the author's website, and are well worth reading sooner than later.  They harmonize well with both "The Knowledge Machine" by Michael Strevens, and "The Book of Why" by Judea Pearl and Dana Mackenzie.

Honestly, though my understanding of "Statistical Rethinking" is largely referential at this point, I am excited by this book the way I was excited when I first stumbled upon "Programming with Standard ML" while semi-exhaustively searching the CS stacks at Bracken Library at Ball State University. Personally, I had difficulty engaging with statistics; I always found the attitude of "the philosophy of statistics is for me but not for thee" that seemed to pervade my (very limited) direct exposure to the subject as a student to be extremely off-putting. It should be noted that never took statistics classes at Case Western Reserve University, which has a wonderful statistics department, so this comment is quite irrelevant to my undergraduate department.  In contrast, this introduction to statistics is grounded in philosophy, which is refreshing.  I see why there is buzz about this book; so thank you, Ozgun Ataman, for recommending it!

These three primary recommendations are all challenging. Most people will require extended study and practice in order to truly make the knowledge your very own. I would still very much recommend reading the preface and first chapter or two of each book sooner than later. If you don't go much deeper, that's okay. I believe referential knowledge very much has value.

It is also important to turn referential knowledge into direct knowledge, analogous to how one might dereference a pointer in the C programming language, or force the evaluation of a suspended computation in the Haskell programming language. I encourage students, especially older children and younger adults, to do deep dives into each of these three books: the initial learning curve may be difficult, but the reward is well worth the effort.

You can't really learn mathematics and computer science without also doing. I strongly encourage students to seek out problem sets they enjoy solving, and also to try creating your own problem sets. I highly recommend "Project Euler".

It's to be expected that you will want and/or need gentler introductions to these books. In preparation for "Proofs and Refutations", George Polya's "How to Solve It" is a classic and popular introduction to basic problem solving heuristics. Or you may find you prefer Polya's  "Mathematics and Plausible Reasoning". I know I found it difficult to stay engaged with "How to Solve It" when I was in high school, because so much of it seemed obvious to me. I probably would have enjoyed "Mathematics and Plausible Reasoning" and would almost certainly have benefitted a great deal from it, especially with a bit of guidance and help.

I do believe that mathematicians and computer programmers, among other professionals, stand to benefit greatly from having higher-quality, more frequent conversations about tradeoffs between problem-solving heuristics. Personally, I've been slow to pick up on the finer points of why heuristics are valuable and interesting. What I've come to deeply appreciate is that heuristics that might be abundantly obvious to some people, are not at all obvious to others. I've been on both sides of that divide, many times. A heuristic that is a good fit for a situation is indispensible, and developing the wisdom to evaluate and choose between heuristics for a given purpose, allows you to accomplish things that can astonish even yourself.

I suspect that many students will appreciate "How to Prove It" by Daniel Velleman as an introduction to "Language, Proof, and Logic", or possibly even a substitute for it. "How to Prove It" provides an introduction to deductive logic with an emphasis on discrete math. Referring to an auxiliary topic, such as discrete math, allows certain issues of syntax and semantics to be treated more informally while still providing a very rigorous introduction to formal deductive logic. I believe many students will prefer this approach, especially if the auxiliary topic is one that the student has a genuine interest in.[^auxiliary-topics-for-deductive-logic]

On the other hand, "Language, Proof, and Logic" provides hints towards model theory. Model theory is a more inward-looking view of the semantics of formal logic itself, with less reference to external ideas. This perspective is an important one, and graduate-level model theory eventually meets up with univeral algebra and algebraic topology. However, the study of formal logic tends to emphasize the aspects of a proof many mathematicians find to be the least interesting. This isolated perspective frequently poses a special challenge to some students, myself included; in these cases "Gödel, Escher, Bach" may be a useful adjunct to "Language, Proof and Logic" for getting comfortable in the foothills of model theory.

For a more comprehensive, up-to-date resource about how to become a logician, I recommend Peter Smith's "Beginning Mathematical Logic: A Study Guide", which is available in digital formats free of charge, as well as inexpensive printed versions. It provides an excellent overview and guide to the modern literature of logic.

[![Good Cop, Pragmatist About the Nature of Truth Cop](external-assets/static.existentialcomics.com/comics/goodCopPragmatistCop1.png)](https://existentialcomics.com/comic/115)
[![Good Cop, Pragmatist About the Nature of Truth Cop](external-assets/static.existentialcomics.com/comics/goodCopPragmatistCop2.png)](https://existentialcomics.com/comic/115)

> So you believe in that garbage, too—theories of knowledge, infinity, laws of probability. I can make no sense of it, and I don't believe you can either, and I don't think your god Peirce knew what he was talking about.
>
> - H.L. Mencken

Charles Sanders Peirce was an American logician and philosopher in the pragmatist school of thought.  He was personally acquainted with William James and Bertrand Russell. He is also known for being an early pioneer in the philosophies of probability, statistics, and inductive logic. In the realm of deductive logic, Peirce's law `((A → B) → A) → A` is equivalent to the law of the excluded middle `A or not A`. Curiously, Scheme's `call-with-current-continuation` operator can be given a type that corresponds to Peirce's law.  This correspondence is part of the Curry-Howard isomorphism, named after Haskell Brooks Curry and William Alvin Howard.  The type theory of the simply typed lambda calculus corresponds to intuitionalistic logic. Thus, adding a typed `call/cc` to the underlying computational calculus results in a type theory that corresponds to classical logic.

* "Mathematics, morally" by Eugenia Chen
* "An Introduction to the Philosophy of Science" by Rudolph Carnap
* "The Knowledge Machine" by Michael Strevens
* "The Road to Reality" by Sir Roger Penrose

[![The Sighting](external-assets/static.existentialcomics.com/comics/platonicNumbers1.jpg)](https://existentialcomics.com/comic/36)
[![The Sighting](external-assets/static.existentialcomics.com/comics/platonicNumbers2.jpg)](https://existentialcomics.com/comic/36)

* "Lectures on the Philosophy of Mathematics" by Joel David Hamkins
* "The Two Cultures of Mathematics" by W. T. Gowers
* "Mathematics: an Experimental Science", by Herbert S. Wilf
* "Enumerative and Algebraic Combinatorics", by Doron Zeilberger
* "Where Mathematics Comes From" by George Lakoff and Rafael E. Núñez
* "The Logical Syntax of Language" by Rudolph Carnap

[![On The Usefulness of Philosophy](external-assets/static.existentialcomics.com/comics/OnTheUsefulnessofPhilosophy.png)](https://existentialcomics.com/comic/408)

* [What is Inductive Logic?](https://www.youtube.com/watch?v=4ZKa1S1wPy4) by Kevin deLaplante
* "The Emergence of Probability", by Ian Hacking
* "Bernoulli's Fallacy: Statistical Illogic and the Crisis of Modern Science", by Aubrey Clayton

* "An Introduction to Probability and Inductive Logic", by Ian Hacking
* "Causal Inference in Statistics: A Primer", by Judea Pearl, Madelyn Glymour, and Nicholas P. Jewell
* "Causality: Models, Reasoning, and Inference", by Judea Pearl
* "Probabilistic Graphical Models", by Daphne Koller and Nir Friedman
* "Introduction to Statistical Inference", by Jack Carl Kiefer
* "Incerto", by Nassim Nicholas Taleb

[![The Three Little Philosophers of Science](external-assets/static.existentialcomics.com/comics/ThreeLittlePhilosophersofScience.png)](https://existentialcomics.com/comic/358)

* "The Logical Foundations of Probability" by Rudolph Carnap
* "Conjectures and Refutations" by Karl Popper
* "The Structure of Scientific Revolutions" by Thomas Kuhn
* "The methodology of scientific research programmes" by Imre Lakatos
* "Against Method" by Paul Feyerabend
* "Representing and Intervening", by Ian Hacking
* "For and Against Method" by Imre Lakatos and Paul Feyerabend, edited by Matteo Moterrelini

Imre Lakatos's philosophy of science and mathematics is a rich source of wisdom, by contrast, Imre Lakatos's life is a rich source of moral refutation. If you'd like to take a close look at the latter half of this dichotomy, I suggest "Chocolate and Chess: Unlocking Lakatos" by Alex Bandy. Do be aware that portions of this book can be rather disturbing, and is best reserved for mature audiences.

[![Fireworks and a theory of language](external-assets/static.existentialcomics.com/comics/FireworksandaTheoryofLanguage.png)](https://existentialcomics.com/comic/381)

[Part II: Deconstructing Bertrand Russell](./Part_02_Deconstructing_Bertrand_Rusell.md)

[^formalizinginformalmath]: Completing the analogy, can informal mathematics be formalized?  Despite being an apparent contradiction in terms, this idea certainly does not seem immediately implausible to me, though I don't know how this idea might be plausible either. I'm not even sure how one might try to proceed if one were to try to write the book on formal informal math. Perhaps it would help if we had more "Proofs and Refutations" style rational reconstructions of the historical development of important mathematical concepts?  That seems potentially quite useful it it's own right, at least. I'm under no illusion that formalizing informal mathematics would eliminate informality: to some degree or another informal mathmatics is unavoidable! Rather, perhaps such an effort would shift the informalities used in practice in useful ways into roles that are hopefully more satisfying and pleasing to the participants involved. Even if such an effort is unworkable, at the very least, informal mathematics and formal mathematics do need to remain well-informed of developments in the each other's fields.

[^auxiliary-topics-for-deductive-logic]: Thus, we should have a banquet of options for learning deductive logic, whether that's the very traditional geometry, or the somewhat more modern logic puzzles, or the relatively recent discrete math, to suit many tastes and interests. There are almost certainly large numbers of alternative auxiliary topics for teaching deductive logic that are worth exploring and developing.