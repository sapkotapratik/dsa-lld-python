- BigO is a way of comparing code one and code two mathematically about how efficient they run.

Time Complexity:
- No of operation involved to complete something.

Space Complexity:
- Amount of memory space it requires for the certain computing problem.


1) Worst Case (Omega):


O(n):

def print_items(n):
    for i in range(n):
        print(i)

print_items(10)

Output: 0 to 9

This ran n time so it's O(n)


2) Drop Constants

def print_items(n):
    for i in range(n):
        print(i)
    
    for j in range(n):
        print(j)

print_items(10)

Output: prints 0 to 9 two times

So it ran n + n time, 2n times so O(2n)
But we can simplify this as O(n).



3) Big O(n ^2)

def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i,j)

Output :

0 0
to
99
Basically 100 items printed out.

which is n*n items printed O(n^2)


4) Drop Non-Dominants:

def print_items(n):
    for i in range(n):
        for j in range(n):
            print(i,j)

    for k in range(n):
        print(k)

print_items(10)

Output:
00
to 
99
and again
0 to 9

So , it's O(n^2) + O(n) = O(n^2 +n) the n becomes insignificant.
Finally, it's O(n^2)