# Shortest-Path-Predictor-for-the-Snakes-and-ladder-Problem-Using-Breadth-First-Search-Algorithm-
<br>
Snakes and Ladder is well known game played by a large population of the world. The unpredictability of this games is what makes it interesting and exciting, however in our research we would to predict the minimum dice moves and the no of turns required for the player. The real challenge is to find the probability for that particular player for winning the game since unpredictable dice numbers can vary the probability of that player. The algorithm used for this research is Breadth First Search(BFS) since BFS has good number of advantages like structure and most importantly finding out all possible paths and picking the shortest path to the goal state. If Snakes and ladder have more than one answer Breadth first search(BFS) will be able to find it.
</br>


<br>
Objectives

->To search for the shortest path to the end in a snakes and ladder game using the breadth first search algorithm and provide the minimum dice moves required to reach the goal state of the game.

->To compute the time and space complexity for finding the shortest path to the goal.

->To calculate the dice number required at each turn of the players to win the game in minimum number of turns.

->To find the probability of winning the game with the minimum number of turns for each player (for two players)

</br>


## Analysis of the Problem
<br>
Snakes and Ladders is a multiplayer game where players use dice rolls to move forward and race to the end and are accompanied by snakes that make you fall back and ladders that boost you up.
A Snakes and Ladders Game can be visualized as matrix with directional linked cells representing the snakes and ladders. Given the starting and ending position the game grid can be traversed to find the shortest path. In doing so the breadth first algorithm can be used.
The problem is to find out the minimum number of moves to play in order to reach the goal from the given starting positions and also find out the dice number required at each move in order to follow this shortest path to the goal.
Each move can have 6 possible options, these can be represented as the 6 children of a node if the game grid is drawn as a tree.

The problem can be viewed as the minimum number of levels in the tree where an end point can be found and which links to travel through in order to reach this endpoint.
The BFS algorithm can be implemented using a Queue. Every time a node of a tree is evaluated, it is popped from the front and all Its children are added at the rear of the queue. In this manner the tree is evaluated level by level with a node and its siblings being evaluated before any of their children.
BFS gives a time complexity of O(N^2)
BFS gives a space complexity of O(N^2)

</br>


## Problem Implementation
<br>
The problem solution is implemented using a matrix to represent the game grid where a cell’s value is -1 is there is no ladder or snakes at that cell. Else the cell’s value equals to the destination of the ladder or snake at that cell.
Each node is implemented using a structure with details like the game cell number, number of dice rolls away from start position and the dice numbers at each roll required to reach this node from the start position.
The algorithm also uses a queue and starts with by enqueuing the given start node. A goal test is run on the first node in the queue, if the test is true the algorithm stops returns the details as the answers. A node is then evaluated , i.e, it is popped out of the queue and all its six children are enqueued.
The details of the children of the node are as follows:
Cell Number: Actual game cell number or the destination of the snake/ladder at that node
Dice rolls: Dice rolls of parent + 1
Dice numbers: Dice numbers of parent appended by dice number required to reach this node from its parent (1 to 6)
In such a manner a node and all its siblings are explored before its children, i.e, the game tree is evaluated level by level.
</br>






