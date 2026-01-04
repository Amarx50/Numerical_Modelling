# Numerical Modelling Projects
This report contains two numerical modelling projects, one solving the Travelling Salesman Problem using Monte Carlo techniques and simulated annealing, and the other investigating the Tacoma Narrows Bridge collapse using coupled differential equations, exploring the Taylor and Cromer methods.

## Travelling Salesman (Monte Carlo)
The Travelling Salesman problem is solved using a simulated annealing algorithm. City coordinates randomly selected, and random swaps are carried out within the connective path. New paths are accepted based on the Metropolis algorithm, with the probability of acceptance being controlled by a temperature schedule that decreases over time. This allows the solution space to be thoroughly explored initially, then as time goes on, convergence into a minima, providing accurate results. 

## Tacoma Narrows Bridge Simulation
The Tacoma Narrows Bridge is modelled using two coupled second-order differential equations. These equations are solved numerically using both the Taylor and Cromer method. Results from the code show that the Taylor method becomes unstable for non-zero initial torsion angles, while the Cromer method provides stable and physically realistic oscillatory behaviour. The model is extended to include an external wind force of the form Asin(ωt), allowing wind amplitude and frequency to be varied.

## Conclusion

In the TSP project, simulated annealing clearly illustrated its use by finding a very accurate
answer to the shortest path between all 30 cities. Whilst this algorithm clearly works better for
smaller sets of data, such as 8 cities, it can still be highly accurate for a larger data set as long as
a suitable number of iterations is used in the model. Downsides of this model were also seen, as
for larger data sets the run-time can be too long for practical use to obtain an accurate solution.
ALso, the algorithm is hard to define as it depends on a lot of parameters, such as the decay
parameter alpha, that changes the results of the algorithm.

For the Tacoma model, it provides a clear insight on which numerical method is suitable for
second order differential equations, which come up all the time in physics. The Cromer-method
is clearly the preferred method, providing a stable and accurate model of the system. Taylor's
method is too unstable, struggling when the intial conditions are not zero, making it unreliable
for a complex simulation such as this one. The integration of wind force into the model gave an
insight to why the bridge collapsed back in 1940. The frequency of the wind matched the natural
frequency of the bridge, and through the various plots we could see the effect this had on the
vertical displacement and the torsion angle as time progressed. At high values of ω, greater than
3, the system clearly shows stable and insignificant oscillations. Whilst results varied slightly,
the key finding was that when ω was between 2.2 and 2.7, the system was unstable and clearly
this was what led to the faliure of the bridge.

Together, these models show how adressing challenging problems requires a lot of work to do -
tweaking parameters to obtain optimal results and refining iterations to obtain reliable solutions
are vital steps to solve complex problems in physics.

## Libraries and Tools
Python, NumPy, Matplotlib

