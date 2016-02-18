# Two Square

A proof of Fermat's theorem on sum of two squares.
It is the proof that uses gaussian integers. This is done in ssreflect.

The final statement reads:

Lemma sum2stest n :
  reflect
  (forall p,  prime p -> odd p -> p %| n -> odd (logn p n) -> p %% 4 = 1)
  (n \is a sum_of_two_square).

