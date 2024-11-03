# CI2024_lab2

I think that a fast approssimate solution can be reached using a greedy algorithm like the ones we have seen in class: the Closer City Algorithm and the Minimum Distance Segments Algorithm. I have implemented my own version of the last one.
Otherwise, to obtain a more accurate solution I have developed a Simulated Annealing Algorithm, that starts from the result of the greedy one.

In the first case, I have noticed that:
  * for very small istances - like Venuatu - both algorithms can lead to the same cost solutions
  * for small istances - like Italy - the Closer City one provides a better solution than the other one
  * for bigger istances - like Russia, Us, China - the second one the brings to the best path
However, I have understood that, even though in a specific case the first greedy algorithm allows to reach a better solution than the second one, it is not convenient to use it to perform the Simulated Annealing, in fact the result is worse than the one reachable strarting from the Minimun Distance Segments Algorithm. I think that that is due to the fact that the tweak used tends to separate some closer cities, so does not fit well together with the mechanism of the first greedy algorithm.

For that reason, I have decided to perform the SA always employing like initial solution the one provided by MDS algorithm.
Then, the Simulated Annealing performs multiple tweaks based on the inversion of a dynamic number of cities in the sequence, I did several trials and I found that an optimum value where to begin is the 60/70% of the total number of cities; this number decreases slowly with each iteration.
Being based on randomic choises, this algorithm provides each time a different solution with a different total cost. I run it some times and I am going to present an average one for each instance, specifying also the values I found reasonable and I have used like restart number and steps. Unfortunately the images are too big so I had to cut them, to better see the 'x' axis it is enought to modify the file name and the parameters, they run in a very fast way.

In each screenshots they are printed in order:
 * the cost of the CCA's solution
 * the cost of the MDSA's solution
 * the best solution gained with the SA

** Vanuatu
restarts: 10 steps: 5

**Italy** restarts: 200 steps: 100

**Russia** restarts: 400 steps: 200

**Us** restarts: 1000 steps: 500

**China** restarts: 2000 steps: 600
