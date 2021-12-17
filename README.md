## A Simplified Wumpus World Simulation in Python

For this project, I aim to simulate the wumpus world where I design an agent to independently navigate the world. For this wumpus there are a few simplifications that were applied. Instead of finding its way back home, the win condition is the agent finding the gold. 

The worlds are designed such that there are no overlaps between wumpuses, pits and gold. The arrow mechanism is also ignored in this world. To start off, we implemented helper functions. We added a Literal class for representation in the KB and wumpus world. It seems cleaner since strings are messier to deal with. The other functions are for finding valud moves, visited cells, and path finding. 

For the path finding, I'm implementing a depth-first search. This is important to simulate the navigation of the agent from its current location to the target location. The dfs function returns a set of paths that the agent will be going through to reach the target location. Depth-first search is used as it simulates the agent's style of navigation which is going deeper into a cell that we have visited instead of checking each neighboring valid and visited cell (this is breadth-first which is not ideal for path finding) 

Next, the KB is designed in such a way that the agent will rule out multiple cells to be visited, safe and risky. More on this will be discussed later.

All in all, the agent will be navigating its own in this Wumpus world and its objective is to keep playing till they die or find the gold. 

