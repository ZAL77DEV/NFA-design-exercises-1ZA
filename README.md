# NFA Design 1

Problems completed: #6, #9, #13, #14, and #15. Alphabet: {0,1}.

## Learning reflection

I will not lie: I chose the easier questions for this assignment so I could finish within the deadline and get comfortable with the basics. One of the harder parts was making sure my test strings were good. I needed shortest, typical, and corner cases, including the empty string, and had to work out the expected accept or reject result before running each test.

Problem #9 required careful attention when tracing multiple paths. For `110`, q0 and q1 are both active after the first `1`. On the second `1`, the old q1 path stops, but q0 creates a new q1 path. That new path reads the final `0` and reaches q2. Keeping track of all active states was the part that required the most care.

The batch tests and the three step traces matched their expected results, so I did not encounter an unexpected result in those runs. The traces helped me understand why a string can be accepted even when another path stops or finishes in a nonfinal state. At least one path must consume the entire string and finish in an accepting state.

For future projects and exams, I will write down the complete set of active states after each symbol instead of following only one path in my head. I will also test empty strings, short strings, boundary cases, and repeated or overlapping patterns. Drawing the computation trees helped me organize the paths and see where each one ended.

I also want to attempt more difficult questions on my own during the week. I know I will not always have a helping hand, so I want to build confidence in working through these problems independently.

## Files and results

Each problem includes a JFLAP machine (`nXX.jff`), a test file (`nXXt.txt`), and a report (`nXXr.md`). The reports contain machine and batch screenshots. Problems #6, #9, and #13 also include handwritten computation trees and step screenshots.

Each machine passed 24 nonempty test strings and a separate empty-string test in JFLAP. Accepted strings appear before rejected strings in each test file.
