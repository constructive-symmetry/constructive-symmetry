[zhuli](https://www.youtube.com/@zhulimath) has a really cool math channel on
youtube with a lot of things that overlap and mesh extremely well with this
project.

The [first video](https://www.youtube.com/watch?v=3B-D3w292TI) is somewhat
similar to what I'd like to touch on in the (very) incomplete script
introducing Pascal's Triangle.  Though I do plan on trying to cover the
multiplicative formula eventually, perhaps in the second video, my first video
is intended to cover the additive method only.

Relative to this presentation, I really want to emphasize relatively principled,
systematic approaches to path generation by using recursive arguments and
hinting at the idea of recursion without belaboring the point.

I want to hint at issues regarding the faithfulness of notation by arguing that
the fact that any difference in the notation used to express the path does
actually lead to a different path.

I want to hint at the fuller principle of inclusion and exclusion, by
emphasizing that the paths that pass through one side of the recursion are
necessarily disjoint from the paths on the other side of the recursion.

In fact I'd like to emphasize both that once the paths are extended, the
last element must differ because the recursive step put it there.  Also,
I'd emphasize that because the unextended paths end up in different locations,
these two sets are necessarily disjoint even before the extension happens.

The [Dark Side of Pascal's Triangle](https://www.youtube.com/watch?v=rQzu5JUjaG0)
is the first video I watched in its entirety. The motivation to cover Pascal's
Triangle as a way of promoting discrete math in the US curriculum, is very much
shared between that project and this project.

It touches on a number of things I had already had planned for the sequel to
KB&SBT. Of course there's a lot of things here I need to learn more properly to
try to organize into some kind of attractive story, some of which I was already
aware of, much of which I was not.

The connections between Stirling numbers and the umbral calculus is totally new
to me, and very interesting!

[What Happens If We Add Fractions Incorrectly](https://www.youtube.com/watch?v=4d6YrTKmjfE)
covers a lot of the material I'd like to eventually cover in this project. The
ordering is very different than what I'm currently thinking; also a few of the
explanations I'm planning are at least somewhat different.  But they appear to
be targetting an audience with some familiarity with vectors, cartesian
coordinates, etc, whereas I am trying to assume less knowledge and
sophistication.

The connection to Simpson's Paradox is one of those obvious-in-retrospect ideas
that I had probably thought about, but for whatever reason wasn't prominent in
my mind. I really like this connection/example, and so I plan on placing it
prominently.

One of the things I like about their approach is that it rather deftly deflects
the standard objection to using `1/0`. However I also think that disarming this
objection in this way runs the risk of opening oneself to a different nonsense
objection: namely the Stern-Brocot tree is unsuitable for children because it
"requires" vectors and/or linear algebra.

Regarding [the argument](https://youtu.be/4d6YrTKmjfE?t=884) that every rational
number appears once and only once in the Farey Sequence: I'm not convinced that
the argument that each number must appear somewhere isn't assuming the
consequent.

I want to be a little bit cautious here because I suspect there are some
more-traditional professors and departments might claim that their uniqueness
argument is also flawed. This is of course not true, but it does depend on a
(co-)inductive proof, the details of which aren't delved into.

That said, I think the uniqueness part of the proof is a-okay, especially in
the overall context. Their existence argument doesn't say anything that is
explicitly incorrect. So am I not familiar with concepts or alternative
viewpoint that would make this outline of an existence proof rigorous?

The two proofs I'm most familiar with are (1) the fact that the Stern-Brocot
tree and the Euclidean algorithm are inverses of each other, a la "Enumerating
the Rationals", (2) a more classical proof employing contradiction that appears
in Concrete Mathematics.

I'm actually *way* more conceptually comfortable with proof (1) than proof (2),
partly because it gives me a useful story in a way I've never quite intuitively
understood from (2). Also, the video seems to tacitly assume (but never prove)
that every element of SL(2,N) appears on the Stern-Brocot tree, i.e. the
less-common direction of the isomorphism between them.

(Incidentally, I also think my preference for the proof based on the Euclidean
algorithm may have something to do with my preferred notions of existence.
[Martin Escardo explains:](https://mathstodon.xyz/@MartinEscardo/115063264039556362)

> Mathematical notions of existence.
>
> 1. Explicit existence: we have one, and here it is for you to see.
> 
> 2. Truncated or anonymous existence: we have one, it doesn't matter what it is, and we won't tell you what it is, not because we are mean, but because we want to emphasize that we don't care which one is chosen.
> 
> 3. Classical existence. It is impossible that it doesn't exist. We won't tell you what it is, not because we are mean, but because we have no clue.

I prefer 1 over 2 over 3. This may in part explain why I tend to latch onto the
proof based on the Euclidean Algorithm.)

The purported existence proof that every rational number appears in the
Stern-Brocot tree I'll rephrase as follows:  Given a rational number `b/a`
and a Farey-like sequence `F_i`, then either `F_i` contains `b/a`, or it would
fall between two fractions `y/x` and `z/w` such that `x*z - y*w = 1`, at
which point you can add terms to the sequence to obtain `F'_i` that contains
`b/a`.

This raises an interesting question in my mind: can you use this information
to quickly derive a continuation of the standard subtraction-based Euclidean
algorithm? The main challenge I see is that you don't have the two running
inputs to the GCD function at the point in time that would correspond to having
the matrix `[x z; y w]` in the accumulator of the extended algorithm, but
this can be recalculated using a bit of linear algebra.

Let's rephrase in terms of the Stern-Brocot representation `SL(2,N) = <L, R>`.
If we affirm the consequent, we know `b/a ≝ [a; b] = LRRLRL...[1; 1]` for some
sequence `S_i` of `L = [1 1; 0 1] ` and `R = [1 0; 1 1] `.  If we know that
`y/x < b/a` and `b/a < z/w`, with `x*z - y*w = 1`, then we know
`P ≝ [x w; y z] ∈ SL(2,N)` and that the Stern-Brocot representation of `P` is a
prefix of `S`.

Thus, given our problem setup, we can write a routine that takes the desired
fraction `b/a` and some boundary fractions `y/x` and `z/w`, computes the
inverse `P'`, and then computes `[a'; b'] ≝ P' [a; b]` and uses that as the
result as part of the continuation of the extended euclidean algorithm on `a`
and `b`.

If one were to write a software routine that would compute this continuation,
we would often want to check at runtime that indeed `y/x < b/a`,  `b/a < z/w`,
and `x*z - y*w = 1`.  Is there any way to say, just do the Linear algebra to
compute `[a'; b']` and then check that everything was okay? Or might it be
necessary to do all that checking up-front?

The answer is, you don't need to check that the target fraction is between
the boundary fractions up-front: you can simply multiply by `P'` and then
check the resulting vector consists of two non-negative integers. I think
you would need to check the determinant is one.