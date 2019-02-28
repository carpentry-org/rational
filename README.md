# rational

Rational numbers (a.k.a fractions) for Carp.

Fractions are expressed as pairs of integers. Mathematical operations and
conversion primitives to and from integers and floating point numbers are
provided.

## Installation

```clojure
(load "git@github.com:carpentry-org/rational@0.1")
```

## Usage

```clojure
(load "rational.carp")

(Rational.new 22 12) ; => (Rational 11/6)
(Rational.* (Rational.new 22 12) (Rational.new 1 6)) ; => (Rational 2/1)
(Rational.to-int (Rational.new 2 1)) ; => 2
(Rational.to-float (Rational.new 1 4)) ; => 0.25
```

Please note that conversion can be lossy, because conversion to integer throws
away any non-real value and conversion to floating point values is only as
accurate as floating point numbers are.

<hr/>

Have fun!
