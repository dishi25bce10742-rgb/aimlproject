# Smart Route Planner
A city route planner that uses classical AI search algorithms (BFS, DFS, and A*) to find the optimal path between cities.
# Smart Route Planner using AI Search Strategies :- 

A city route planner that uses classical AI search algorithms (BFS, DFS, and A*) 
to find the optimal path between cities. 

##  Real-World Problem

Every day, millions of people need to navigate routes from one place to another. Apps like Google Maps solve this using intelligent search, not by checking every possible route, but by using smart strategies that prioritize the most promising paths first.

This project simulates that exact problem on a real Indian city road network, and 
compares three AI search strategies to show why A* is the most efficient.

## AI Concepts Used

 Concept  and How it's applied 

Intelligent Agent - The route planner is a goal-based agent that perceives start/goal cities and acts by returning the best route 
PEAS Model - Performance: shortest distance. Environment: city road graph. Actuators: route output. Sensors: user city input 
BFS - Explores all cities level by level and guarantees fewest stops 
DFS - Explores deep paths first (not optimal), shown for comparison 
A* Search - Uses Haversine distance as admissible heuristic, guarantees shortest distance with fewest nodes explored 
Heuristic - Straight-line (Haversine) distance between cities, never overestimates, so A* remains optimal 

##  Project Structure 
route-planner/

route_planner.py   # Main code — graph, algorithms, agent

README.md

## Getting Started
Bash:-
# 1. Clone the repo
git clone https://github.com/dishi25bce10742-rgb/aimlproject.git

cd aimlproject
# 2. No external libraries needed — uses Python stdlib only
python Main Code.py

##  City Network
The map covers 10 major cities in Madhya Pradesh, India connected by real road distances:

Bhopal, Indore, Jabalpur, Gwalior, Ujjain, Sagar, Rewa, Satna, Dewas, Chhindwara

##  Algorithm Comparison

For the route - Indore → Jabalpur:

| Algorithm | Distance | Stops | Nodes Explored |
| BFS       | 525 km  | 2     | 7              |
| DFS       | 385 km  | 2     | 3              |
| A*        | 385 km  | 2     | 3              |

> A* finds the same optimal route as BFS but explores fewer nodes — 
> this is the power of a good heuristic.

##  Why A* Wins
BFS ignores actual distances

DFS may give suboptimal results

A* combines:
f(n) = g(n) + h(n)
g(n): distance travelled
h(n): estimated distance (Haversine)

Heuristic is admissible → guarantees optimal path


