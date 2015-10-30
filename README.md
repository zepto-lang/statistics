# statistics

A minimal statistics library in zepto. It is in alpha right now.

## Usage

It implements the same interface as the Python
[statistics standard library](https://docs.python.org/3/library/statistics.html)
and is more or less a direct port (except for the `mode` function, for which I
could not find a straightforward equivalent).

Using it could look like this:
```clojure
(load "statistics.zp")
(define mean (import "statistics:mean"))
(define pstdev (import "statistics:pstdev"))
(define variance (import "statistics:variance"))
(define data [1.5 2.5 2.5 2.75 3.25 4.75])
(pstdev data) ; => 0.986893273527251
(pstdev data (mean data)) ; => 0.986893273527251 ; avoids recalculating the mean
(variance [2.75 1.75 1.25 0.25 0.5 1.25 3.5]) ; => 1.3720238095238095
```

## Testing

The test file assumes to be run with the `zepto_tests` utility script.

<br/>

*Have fun!*
