Test Not the Truth
==================

Suppose we have the following definition and assignment:

    classify <- function ( value , thresholds ) {
            stopifnot (
                is.numeric ( value ) ,
                length ( value ) == 1 ,
                is.numeric ( thresholds ) ,
                ! is.unsorted ( thresholds ) )
            if ( value < thresholds [ 1 ] ) {
                return ( 1 )
            } else if ( thresholds [ 1 ] <= value && value < thresholds [ 2 ] ) {
                return ( 2 )
            } else return ( 3 ) }

What's wrong with the definition?

The test `thresholds [ 1 ] <= value` cannot possibly be `FALSE`.
Once the evaluation of the function proceeds to the `else if`,
it has already been determined that `value < thresholds [ 1 ]`.
Therefore is is impossible for `thresholds [ 1 ] <= value` to
be `FALSE`.

The above definition of `classify` goes agains two of Leo
Brodie's \[THIN4\] tips (Nos. 8.4 and 8.15):

> Don't test for something that has already been excluded

> Don't test for something that can't possibly happen

Applying the principle, a better definition of `classify` would be:

    classify <- function ( value , thresholds ) {
            stopifnot (
                is.numeric ( value ) ,
                length ( value ) == 1 ,
                is.numeric ( thresholds ) ,
                ! is.unsorted ( thresholds ) )
            if ( value < thresholds [ 1 ] ) {
                return ( 1 )
            } else if ( value < thresholds [ 2 ] ) {
                return ( 2 )
            } else return ( 3 ) }
            
We might opt for the terser:

    classify <- function ( value , thresholds ) {
            stopifnot (
                is.numeric ( value ) ,
                length ( value ) == 1 ,
                is.numeric ( thresholds ) ,
                ! is.unsorted ( thresholds ) )
            if ( value < thresholds [ 1 ] ) return ( 1 ) else
            if ( value < thresholds [ 2 ] ) return ( 2 ) else
            return ( 3 ) }

The visual alignment of the `if` phrases makes it easier to
see their differences.

References
----------

\[THIN4\] Brodie L (2004) _Thinking Forth: A Language and Philosophy for
Solving Problems_. ISBN:0976458705.
http://thinking-forth.sourceforge.net/
