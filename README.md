# Travelling Salesman Problem

### What is it?
It is a problem in which we need to complete a cycle passing through a set of points, being each of them separated from each others a know distance, without repeating any point and returning to the origin once all points has been visited.

A clear example is the <a href="https://en.wikipedia.org/wiki/Travelling_salesman_problem">Travelling Salesman Problem</a>: Suppose there are several locations in a city that need to be visited, being each one separated from the other ones a known distance (that we can store in a distance matrix). The objective is to complete the cycle following the optimal path, the one which minimize the traversed distance.

In order to solve this problem, I have used the Held-Karp algorithm.

### What is in the repository? 

The repository contains:

  <b>A) "Example":</b> An example of a distance matrix.
  <br>
  <b>B) "HK_Paths":</b> First implementation of the algorithm, which allow us all the posibilities with their distances.
  <br>
  <b>C) "HK_Optimal":</b> Second implementation of the algorithm, which do not show all the options, but is more efficient.

### How is the algorithm?
The Held-Karp algorithm is a brute search algorithm which belong to the family of the "branch and bound" ones.

An algorithm that belongs to the <a href="https://en.wikipedia.org/wiki/Branch_and_bound">Branch and bound</a> family is used to solve problems where we could obtain an optimal solution given a set of possible solutions. The algorithm will evaluate all the possible alternatives, keeping the best one and using it as a threshold to improve.

This would be an example of the use of Held-Karp to this problem:
<br><br>
<img align="center" src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Branchbound.gif">

### Special considerations:
* It is important to recall that <b>the distance A-B could be different from the distance B-A</b> (imagine a one-way street, going in one direction is shorter that the opposite).
<br><br>
* <b>It does not matter which is the starting point,</b> because at the end the cycle will cover all the locations, the result would be the same starting at any othe location.
<br><br>
* <b>This problem needs big computational capacity.</b> With each new location, the time to calculate the optimal solution increase exponentially (with more that 12 locations could be a nightmare).
