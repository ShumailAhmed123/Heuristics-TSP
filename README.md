# Held-Karp

### What is it?
The Held-Karp algorithm is a brute search algorithm which belong to the family of the "branch and bound" ones.

An algorithm that belongs to the <a href="https://en.wikipedia.org/wiki/Branch_and_bound">Branch and bound</a> family is used to solve problems where we could obtain an optimal solution given a set of possible solutions. The algorithm will evaluate all the possible alternatives, keeping the best one and using it as a threshold to improve.

### What is in the repository? 

The repository contains:

  <b>A) "Example":</b> An example of a distance matrix.
  <br>
  <b>B) "HK_Paths":</b> First implementation of the algorithm, which allow us all the posibilities with their distances.
  <br>
  <b>C) "HK_Optimal":</b> Second implementation of the algorithm, which do not show all the options, but is more efficient.

### To which problems could it be applied?
The problem in which I used this algorithm is the following:

Suppose you have several locations in a city, being each one separated from the other ones a known distance, different from each location. We can built a distances matrix to store all the distances between any pair of points. Now suppose that we want to visit every different location starting at a specific point, without repeating any of the locations, and returning to the starting point at the end (completing a cycle). This problem is called <a href="https://en.wikipedia.org/wiki/Travelling_salesman_problem">Travelling Salesman Problem</a>.

<img align="center" src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Branchbound.gif">

### Special considerations:
* It is important to recall that <b>the distance A-B could be different from the distance B-A</b> (imagine a one-way street, going in one direction is shorter that the opposite).
* <b>It does not matter which is the starting point,</b> because at the end the cycle will cover all the locations, the result would be the same starting at any othe location.
* <b>This problem needs big computational capacity.</b> With each new location, the time to calculate the optimal solution increase exponentially (with more that 12 locations could be a nightmare).
