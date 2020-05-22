#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
This loop will always run N times, since we increment by n*n each loop, and the goal is to reach (n*n) * n. The run time is O(N)

b)
The inner while loop is repeatedly doubling its value to reach n, this is akin to something like a binary search repeatedly halving its value. This makes the inner while loop O(logN) runtime complexity. Considering this operation has to happen range(n) times due to the outer for loop, the final complexity is N(logN).

c)
This recursive function simply decrements by 1 and reruns itself. It can only run as many times as the original bunnies parameter that is inputted. This gives O(N) runtime complexity.

## Exercise II

For determining the maximum floor we can drop an egg from a building and have it not break, we must have a system to test the floors of each new building we come across. To break the least amount of eggs before locating floor F, the peak floor the egg will remain intact, we must do the following code;


function breakPoint(numberOfFloors)
    midFloor = n // 2

    dropTheEgg() 
    If it breaks: Check whether it breaks on the floor immediately below

        Does it break one floor below?: 
        (Yes): Rerun recursively on the lower half of this range | breakPoint(midFloor // 2)
        
        (No): You have found the max floor it won't break, | return (n-1)

    If it doesn't break:

        Does it break one floor above?:
        (Yes): You have found the max floor it won't break | return(n)

        (No): rerun recursively on the upper half of this range | breakPoint(midpoint + midpoint // 2)

This being essentially a binary search tree, the runtime will be O(logN)