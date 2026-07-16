# rational

Rational numbers (a.k.a fractions) for Carp.

Fractions are expressed as pairs of integers. Mathematical operations and
conversion primitives to and from integers and floating point numbers are
provided.

## Installation

```clojure
(load "git@github.com:carpentry-org/rational@0.7.0")
```

## Usage

```clojure
(load "git@github.com:carpentry-org/rational@0.7.0")

(Rational.new 22 12) ; => (Rational 11/6)
(Rational.mul (Rational.new 22 12) (Rational.new 1 6)) ; => (Rational 2/1)
(Rational.to-int (Rational.new 2 1)) ; => 2
(Rational.to-float (Rational.new 1 4)) ; => 0.25
(Rational.rationalize 3.14159 300) ; => (Rational 355/113)
(Rational.floor (Rational.new 7 2)) ; => (Rational 3/1)
(Rational.ceil (Rational.new 7 2)) ; => (Rational 4/1)
(Rational.round (Rational.new 7 2)) ; => (Rational 4/1)
(Rational.reciprocal (Rational.new 3 4)) ; => (Rational 4/3)
(Rational.pow (Rational.new 2 3) 3) ; => (Rational 8/27)
(Rational.pow (Rational.new 2 3) -2) ; => (Rational 9/4)
(Rational.sign (Rational.new -3 4)) ; => (Rational -1/1)
(Rational.pos? (Rational.new -3 4)) ; => false
(Rational.neg? (Rational.new -3 4)) ; => true
(Rational.zero? (Rational.new 0 5)) ; => true
(Rational.<= (Rational.new 1 2) (Rational.new 2 3)) ; => true
(Rational.min (Rational.new 1 2) (Rational.new 2 3)) ; => (Rational 1/2)
(Rational.max (Rational.new 1 2) (Rational.new 2 3)) ; => (Rational 2/3)
(Rational.clamp (Rational.new 0 1) (Rational.new 1 1) (Rational.new 3 2)) ; => (Rational 1/1)
```

Please note that conversion can be lossy, because conversion to integer throws
away any non-real value and conversion to floating point values is only as
accurate as floating point numbers are.

<hr/>

Have fun!
