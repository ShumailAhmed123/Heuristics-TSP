# Held-Karp

### What is it?
The Held-Karp algorithm is a brute search algorithm which belong to the family of the "branch and bound" ones.

An algorithm that belongs to the "Branch and bound" is used to solve problems where we could obtain an optimal solution given a set of possible solutions. The algorithm will evaluate all the possible alternatives, keeping the best one and using it as a threshold to improve.

### What is in the repository? 

The repository contains:

  A) An example of a distance matrix.
  
  B) First implementation of the algorithm, which allow the user to see all the posibilities with their distances. ("HK_Paths")
  
  C) Second implementation of the algorithm, which do not show all the options, but is quite more efficient. ("HK_Optimal")

### To which problems could it be applied?
The problem in which I used this algorithm is the following:

Suppose you have several locations in a city, being each one separated from the other ones a known distance, different from each location. We can built a distances matrix to store all the distances between any pair of points. Now suppose that we want to visit every different location starting at a specific point, without repeating any of the locations, and returning to the starting point at the end (completing a cycle). This problem is called <a href="https://en.wikipedia.org/wiki/Travelling_salesman_problem">Travelling Salesman Problem</a> for obvious reasons.

### Special considerations:
* It is important to recall that the the distance A-B could be different from the distance B-A (imagine a one-way street, going in one direction is shorter that the opposite).
* It does not matter which is the starting point, because at the end the cycle will cover all the locations, the result would be the same starting at any othe location.
* This problem needs big computational capacity. With each new location, the time to calculate the optimal solution increase exponentially (with more that 12 locations could be a nightmare).
