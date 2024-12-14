In the notes to commit 5b981f5300f8eab18cfb73cc7c083fae8bb6214f, I
noted what seemed like a contradiction in these two sources:

https://math.stackexchange.com/questions/2433055/group-isomorphic-to-its-automorphism-group

https://math.stackexchange.com/questions/1008972/the-automorphism-group-of-the-infinite-dihedral-group

In previous versions of the notes associated with this project, I'd tacitly
assumed that Dih(Z) ≅ Aut(Dih(Z)), based on the first source.  But I didn't
(and still don't quite) correctly understand the automorphisms of Dih(Z), which
turn out to be a little tricker than I thought.

The latter is clearly correct regarding Inn(Dih(Z)), and is clearly correct
regarding the existence of an outer automorphism, and has the sheen of
correctness with respect to the claim that Out(Dih(Z)) ≅ Z_2.

    Since
          Aut(Dih(Z)) ≅ Inn(Dih(Z)) ⋊ Z_2
      and     Dih(Z)  ≅ Inn(Dih(Z))

I assumed that the difference on the right hand side implied that Dih(Z) cannot
be isomorphic to Aut(Dih(Z)).  However, because we are dealing with an infinite
group, it should be possible that Inn(Dih(Z)) ≅ Inn(Dih(Z)) ⋊ Z_2

I realized this after I looked somewhat more carefully at "A Note on Groups with
Just-Infinite Automorphism Groups", by Francesco de Giovanni and Diana
Imperatore, noticed that it acknowledged that Dih(Z) had outer automorphisms,
and concluded that I was likely incorrect about the paper being wrong
because it was much too basic a mistake for a reputable mathematician
who specializes in Group Theory to plausibly make.

https://groupprops.subwiki.org/wiki/Dihedral_group:D12

On the other hand, the page above is definitely incorrect: Dih(Z_6) cannot
be complete because it has a non-trivial center.  The same is true of all
dihedral groups of even degree. (or whose order is a multiple of four)

Is Dih(Z_6) actually isomorphic to Aut(Dih(Z_6))?

Can I demonstrate

    Inn(Dih(Z)) ≅ Inn(Dih(Z)) ⋊ Z_2
