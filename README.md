# learning-python

Following *Python Crash Course, 2nd Ed.* to learn Python.

----------------------------------------------------

Following Coursera course "Python for DS & AI"

Tuples are immutable.
Tuples can be nested.

## Lists

Lists are mutable.
```
lst.extend(["new","elements"]) // concatenates
lst.append(["new","elements"]) // appends rather than concatenates (only one new element)
del(lst[0]) // removes first element of the list
"hard rock".split() // returns ["hard", "rock"]
"A,B,C,D".split(",") // returns ["A", "B", "C", "D"]
```

List aliasing:
```
A = ["hard rock", 10, 1.2]
B = A
// now A, B reference the same memory
A[0] = "hard rock" // will change A and B
// Cloning instead of aliasing will avoid this problem
B = A[:]
```
