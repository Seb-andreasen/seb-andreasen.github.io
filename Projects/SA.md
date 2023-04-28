## Simulated Annealing - Prescriptive analysis

**Project description:** 
Predictive analytics using AI/ML can answer the question "what will happen?", while prescriptive analytics can provide insights on "what should we do about it?"

For instance, ML can be used to predict traffic levels in a given area, but what should we do about it? Prescriptive analytics can help minimize this decision space and facilitate better decisions.

### 1. The example - Finding the fastest route around the world

To illustrate, consider this example of finding the fastest (near) optimal route to visit all countries in the world, with the constraint of only being able to visit a continent once.

To solve this, I used the metaheuristic called Simulated Annealing to investigate the search-space for near optimal solutions.

### 2. The analysis and the solution

In short, the algorithm finds a solution, makes a small change to the solution and tests whether or not the new solution is better than the previous one and then continues for a given amount of time.

In this case I made the search two-fold by first finding the optimal order to visit each continent and then the optimal route within each continent. 

In less than a minute it was possible to reduce the total distance travelled by 45%.
<br><br>

<img src="/images/map.gif?raw=true"/>

<br><br>

### 3. Future work

Imagine how the same techniques can be applied to areas such as supply chain planning, time table scheduling, factory layouts, traffic planning, etc., etc.
