<!---
This file was generated from `meta.yml`, please do not edit manually.
Follow the instructions on https://github.com/coq-community/templates to regenerate.
--->
# twoSquare

[![Docker CI][docker-action-shield]][docker-action-link]

[docker-action-shield]: https://github.com/thery/twoSquare/actions/workflows/docker-action.yml/badge.svg?branch=master
[docker-action-link]: https://github.com/thery/twoSquare/actions/workflows/docker-action.yml





A proof of Fermat's theorem on sum of two squares.
It is the proof that uses gaussian integers. This is done in ssreflect.
It contains two files :

********************************

gauss_int.v : the definition of gaussian integers

fermat2.v : the proof of Fermat's theorem

********************************

The final statement reads:

From mathcomp.contrib.sum_of_two_square
Require Import fermat2.

Check sum2stest.

sum2stest :

reflect
    (forall p,  prime p -> odd p -> p %| n -> odd (logn p n) -> p %% 4 = 1)
    (n is a sum_of_two_square).

## Meta

- Author(s):
  - Laurent Théry
- License: [MIT License](LICENSE)
- Compatible Rocq/Coq versions: 9.0 or later
- Additional dependencies:
  - [MathComp ssreflect 2.4 or later](https://math-comp.github.io)
  - [MathComp algebra 2.4 or later](https://math-comp.github.io)
  - [MathComp field 2.4 or later](https://math-comp.github.io)
- Rocq/Coq namespace: `twoSquare`
- Related publication(s): none

## Building and installation instructions

To build and install manually, do:

``` shell
git clone https://github.com/thery/twoSquare.git
cd twoSquare
make   # or make -j <number-of-cores-on-your-machine> 
make install
```



