# Artificial-intelligence
Artificial Intelligence is a vast field encompassing issues that require more space than a single book on the topic. With inspiration from multiple fields of knowledge such as neurology, psychology, philosophy and literature to say the least; artificial intelligence is an amalgamation of yet more refined subjects which are briefly described in this book. The authors of this book have tried their best to provide you with the most relevant and accurate information presently available. Please feel free to discuss on this book's discussion page.

Applications of AI
AI has a wide spectrum of applications including natural language processing, search engines, medical diagnosis, bioinformatics and cheminformatics, detecting credit card fraud, stock market analysis, classifying DNA sequences, speech and handwriting recognition, object recognition in computer vision, game playing, machine learning and robot locomotion.

Some scientists and Futurologists predict that in near future AI will make digital human, artificial life and artificial immortality possible.
What is A.I.?
There are numerous definitions of what artificial intelligence is.

We end up with four possible goals:

Systems that think like humans (focus on reasoning and human framework)
Systems that think rationally (focus on reasoning and a general concept of intelligence)
Systems that act like humans (focus on behavior and human framework)
Systems that act rationally (focus on behavior and a general concept of intelligence)
What is rationality? -> "doing the right thing" - simply speaking.

Definitions:

For (1.): "The art of creating machines that perform functions that require intelligence when performed by humans" (Kurzweil). Involves cognitive modeling - we have to determine how humans think in a literal sense (explain the inner workings of the human mind, which requires experimental inspection or psychological testing)

For (2.): "GPS - General Problem Solver" (Newell and Simon). Deals with "right thinking" and dives into the field of logic. Uses logic to represent the world and relationships between objects in it and come to conclusions about it. Problems: hard to encode informal knowledge into a formal logic system and theorem provers have limitations (if there's no solution to a given logical notation).

For (3.): Turing defined intelligent behavior as the ability to achieve human-level performance in all cognitive tasks, sufficient to fool a human person (Turing Test). Physical contact to the machine has to be avoided, because physical appearance is not relevant to exhibit intelligence. However, the "Total Turing Test" includes appearance by encompassing visual input and robotics as well.

For (4.): The rational agent - achieving one's goals given one's beliefs. Instead of focusing on humans, this approach is more general, focusing on agents (which perceive and act). More general than strict logical approach (i.e. thinking rationally).

Strong AI vs. Weak AI
Strong AI = machine-based artificial intelligence that can truly reason and becomes self-aware (sentient), either human-like (thinks and reasons like a human mind) or non-human-like (different form of sentience and reasoning) - coined by John Searle: "an appropriately programmed computer IS a mind" (see Chinese Room Experiment).
Weak AI = machine-based artificial intelligence that can reason and solve problems in a limited domain. Hence it acts as if it were intelligent in that domain, but would not be truly intelligent or sentient.
Turing Test
A human judge engages in a natural language conversation with two other parties, one a human and the other a machine; if the judge cannot reliably tell which is which, then the machine is said to pass the test. It is assumed that both the human and the machine try to appear human.

Objections
A machine passing the test could simulate human behavior, but this might be considered much weaker than intelligence - the machine might just follow a set of cleverly designed rules. Turing rebutted this by saying that maybe the human mind is just following a set of cleverly designed rules as well.
A machine could be intelligent without being capable of conducting conversations with humans
Many humans might fail this test, if they're illiterate or inexperienced (e.g. children)
Chinese Room Experiment
Tried to debunk the claims of "Strong AI". Searle opposed the view that the human mind IS a computer and that consequently, any appropriately construed computer program could also be a mind.

Outline
A man who doesn't speak Chinese sits in a room and is handed sheets of paper with Chinese symbols through a slit. He has access to a manual with a comprehensive set of rules on how to respond to this input. Searle argues, that even though he can answer correctly, he doesn't understand Chinese; he's just following syntactical rules and doesn't have access to the meaning of them. Searle believes that "mind" emerges from brain functions, but is more than a "computer program" - it requires intentionality, consciousness, subjectivity and mental causation.

Mind-Body Problem
The problem deals with the relationship between mental and physical events. Suppose I decide to stand up. My decision could be seen as a mental event. Now something happens in my brain (neurons firing, chemicals flowing, you name it) which could be seen as a physical, measurable event. How can it be, that something "mental" causes something "physical". Hence it's hard to claim that both are completely different things. One could go on and claim that these mental events are, in fact, physical events: My decision is neurons firing, but I'm not aware of this - I feel like I made a decision independently from the physical. Of course this works the other way round too: everything physical could, in fact, be mental events. When I stand up after having made the decision (mental event), I'm not physically standing up, but my actions cause mental events in my and the bystanders minds - physical reality is an illusion.

Frame Problem
It is the question of how to determine which things remain the same in a changing environment.

Problem-Solving
Occurs whenever an organism or artificial intelligence is at some current state and does not know how to proceed in order to reach a desired goal state. This is considered to be a problem that can be solved by coming up with a series of actions that lead to the goal state (the "solving").

Search
Overview
In general, search is an algorithm that takes a problem as input and returns with a solution from the searchspace. The search space is the set of all possible solutions. We dealt a lot with so called "state space search" where the problem is to find a goal state or a path from some initial state to a goal state in the state space. A state space is a collection of states, arcs between them and a non-empty set of start states and goal states. It is helpful to think of the search as building up a search tree - from any given node (state): what are my options to go next (towards the goal), eventually reaching the goal.

Uninformed Search
Uninformed search (blind search) has no information about the number of steps or the path costs from the current state to the goal. They can only distinguish a goal state from a non-goal state. There is no bias to go towards the desired goal.

For search algorithms, open list usually means the set of nodes yet to be explored and closed list the set of nodes that have already been explored.

Breadth-First-Search
Starts with the root node and explores all neighboring nodes and repeats this for every one of those (expanding the "depth" of the search tree by one in each iteration). This is realized in a FIFO queue. Thus, it does an exhaustive search until it finds a goal.
BFS is complete (i.e. it finds the goal if one exists and the branching factor is finite).
It is optimal (i.e. if it finds the node, it will be the shallowest in the search tree).
Space: {\displaystyle O(b^{d})} {\displaystyle O(b^{d})}
Time: {\displaystyle O(b^{d})} {\displaystyle O(b^{d})}
Depth-First-Search
Explores one path to the deepest level and then backtracks until it finds a goal state. This is realized in a LIFO queue (i.e. stack).
DFS is complete (if the search tree is finite) and incomplete (if the search tree is infinite)
It is not optimal (it stops at the first goal state it finds, no matter if there is another goal state that is shallower than that).
Space: {\displaystyle O(bm)} {\displaystyle O(bm)} (much lower than BFS).
Time: {\displaystyle O(b^{m})} {\displaystyle O(b^{m})} (Higher than BFS if there is a solution on a level smaller than the maximum depth of the tree).
Danger of running out of memory or running indefinitely for infinite trees.
Depth-Limited-Search / Iterative Deepening
To avoid that, the search depth for DFS can be either limited to a constant value, or increased iteratively over time, gradually increasing the maximum depth to which it is applied. This is repeated until finding a goal. Combines advantages of DFS and BFS.
ID is complete.
It is optimal (the shallowest goal state will be found first, since the level is increased by one every iteration).
Space: {\displaystyle O(bd)} {\displaystyle O(bd)} (better than DFS, d is depth of shallowest goal state, instead of m, maximum depth of the whole tree).
Time: {\displaystyle O(b^{d})} {\displaystyle O(b^{d})}.
Bi-Directional Search
Searches the tree both forward from the initial state and backward from the goal and stops when they meet somewhere in the middle.
It is complete and optimal.
Space: {\displaystyle O(b^{d/2})} {\displaystyle O(b^{d/2})}.
Time: {\displaystyle O(b^{d/2})} {\displaystyle O(b^{d/2})}.
Informed Search
In informed search, a heuristic is used as a guide that leads to better overall performance in getting to the goal state. Instead of exploring the search tree blindly, one node at a time, the nodes that we could go to are ordered according to some evaluation function {\displaystyle h(n)} {\displaystyle h(n)} that determines which node is probably the "best" to go to next. This node is then expanded and the process is repeated (i.e. Best First Search). A* Search is a form of BestFS. In order to direct the search towards the goal, the evaluation function must include some estimate of the cost to reach the closest goal state from a given state. This can be based on knowledge about the problem domain, the description of the current node, the search cost up to the current node BestFS optimizes DFS by expanding the most promising node first. Efficient selection of the current best candidate is realized by a priority queue.

Greedy Search:
Minimizes the estimated cost to reach the goal. The node that is closest to the goal according to {\displaystyle h(n)} {\displaystyle h(n)} is always expanded first. It optimizes the search locally, but not always finds the global optimum.
It is not complete (can go down an infinite branch of the tree).
It is not optimal.
Space: {\displaystyle O(b^{m})} {\displaystyle O(b^{m})} for the worst case.
Same for time, but can be reduced by choosing a good heuristic function.
A* Search:
Combines uniform cost search (i.e. expand node on path with lowest cost so far) and greedy search. Evaluation function is {\displaystyle f(n)=g(n)+h(n)} {\displaystyle f(n)=g(n)+h(n)} (or estimated cost of the cheapest solution through node n). It can be proven that A* is complete and optimal if {\displaystyle h} h is admissible - that is, if it never overestimates the cost to reach the goal. This is optimistic, since they think the cost of solving the problem is less than it actually is.
Examples for {\displaystyle h} h:
Path-Finding in a map: Straight-Line-Distance.
8-Puzzle: Manhattan-Distance to Goal State.
Everything works, it just has to be admissible (e.g. {\displaystyle h(n)=0} {\displaystyle h(n)=0} always works, but transforms A* back to uniform cost search).
If a heuristic function {\displaystyle h_{1}} {\displaystyle h_{1}} estimates the actual distance to the goal better than another heuristic function {\displaystyle h_{2}} {\displaystyle h_{2}}, then {\displaystyle h_{1}} {\displaystyle h_{1}} dominates {\displaystyle h_{2}} {\displaystyle h_{2}}.
A* maintains an open list (priority queue) and a closed list (visited nodes). If a node is expanded that's already in the closed list, stored with a lower cost, the new node is ignored. If it was stored with a higher cost, it is deleted from the closed list and the new node is processed.
{\displaystyle h} h is monotonic, if the difference between the heuristics of any two connected nodes does not overestimate the actual distance between those nodes. Example of a non-monotonic heuristic: {\displaystyle n} n and {\displaystyle n'} {\displaystyle n'} are two connected nodes, where {\displaystyle n} n is the parent of {\displaystyle n'} {\displaystyle n'}. Suppose {\displaystyle g(n)=3} {\displaystyle g(n)=3} and {\displaystyle h(n)=4} {\displaystyle h(n)=4}, then we know that the true cost of a solution path through {\displaystyle n} n is at least 7. Now suppose that {\displaystyle g(n')=4} {\displaystyle g(n')=4} and {\displaystyle h(n')=2} {\displaystyle h(n')=2}. Hence, {\displaystyle f(n')=6} {\displaystyle f(n')=6}.
First off, the difference in the heuristics (that is, 2) overestimates the actual cost between those nodes (which is 1).
However, we know that any path through {\displaystyle n'} {\displaystyle n'} is also a path through {\displaystyle n} n and we already know that any path through {\displaystyle n} n has a true cost of at least 7. Thus, the f-value of 6 for {\displaystyle n'} {\displaystyle n'} is meaningless and we will consider its parent's f-value.
{\displaystyle h} h is consistent, if the h-value for a given node is less or equal than the actual cost from this node to the next node plus the h-value from this next node (triangular inequality).
If {\displaystyle h} h is admissible and monotonic, the first solution found by A* is guaranteed to be the optimal solution (open/close list bookkeeping is no longer needed).
Finding Heuristics:

Relax the problem (e.g. 8-puzzle: Manhattan distance).
Calculate cost of subproblems (e.g. 8-puzzle: calculate cost of first 3 tiles).
Adversarial Search (Game Playing)
Minimax is for deterministic games with perfect information. Non-deterministic games will use the expectiminimax algorithm.

Minimax Algorithm:
A two player zero-sum game, in which both players make a move alternately, is defined by an initial state (e.g. board positions), a set of operators that define legal moves, a terminal test that defines the end of the game and a utility function that determines a numeric value for the outcome of the game (e.g. "1" for win, "-1" for loss).
If it was a search problem, one would simply search for a path that leads to a terminal state with value "1". But the opponent (Min) will try to minimize one's (Max's) outcome. The minimax algorithm generates the whole game tree and applies the utility function to each terminal state. Then it propagates the utility value up one level and continues to do so until reaching the start node.
Propagation works like this: Min is assumed to always choose the option that is the worst for Max (minimum utility value). If one has three terminal states in one branch with 1, 2 and 3 as their utility values, then Min would choose 1. Hence, "1" is propagated to the next level and so forth. Max can then decide upon his opening move on the top level (the "minimax decision" = maximizing utility under the assumption that the opponent will play perfectly to minimize it).
For games that are too complex to compute the whole game tree, the game tree is cut off at some point and the utility value is estimated by a heuristic evaluation function (e.g. "material value" in chess).
Alpha-Beta Pruning
We don't have to look at each node of the game tree: Minimax with alpha-beta pruning yields the same result as a complete search, but with much greater efficiency (reduces its effective branching factor to its square root).
Here we store the best value for Max' play found so far in alpha and the best value for Min's play found so far (i.e. the lowest value) in beta.
If, at any given point, alpha becomes smaller than beta, we can prune the game tree at this point. Therefore, it is required to evaluate at least on set of leaf nodes branching off of one of the deepest Min nodes and then use the acquired alpha-value to prune the rest of the search.
Chance:
Introduces "chance nodes" to the decision points, based on what kind of chance is introduced (e.g. a 50/50 chance for flipping a coin), which yield the "expected value" (average - add up utility values weighted by the chance to achieve them).
Example: 3 leaf nodes, values 5, 6 and 10 = 21 altogether - the chance to get to any one of them is 1/3 - hence the expected value is {\displaystyle 21*1/3=7} {\displaystyle 21*1/3=7}
Constraint Satisfaction Problems
For CSPs, states in the search space are defined by the values of a set of variables, which can get assigned a value from a specific domain, and the goal test is a set of constraints that the variables must obey in order to make up a valid solution to the initial problem.

Example: 8-queens problem; variables could be the positions of each of the eight queens, the constraint to pass the goal test is that no two queens can be such that they harm each other.

Different types of constraints:

unary (value of a single variable)
binary (pairs of variables, e.g. x > y)
n-ary
In addition to that, constraints can be absolute or preference (the former rules out certain solutions, the latter just says which solutions are preferred). The domain can be discrete or continuous. In each step of the search, it is checked if any variable has violated one of the constraints - if yes: backtrack and rule out this path.

Forward checking checks if any decisions on yet unassigned variables would be ruled out by assigning a value to a variable. It deletes any conflicting values from the set of possible values for each of the unassigned variables. If one of the sets becomes empty - backtrack immediately.

There are also heuristics for making decisions on variable assignments.

Selecting the next variable:

Most-constrained-variable works together with forward checking (checking which values are still allowed for each unassigned variable)
the next variable to be assigned a value is the one with the fewest possible values (reduces branching factor).
Most-constraining-variable assigns a value to the variable that is involved in the largest number of constraints on other yet unassigned variables.
After selecting the variable:

Least-constraining-value assigns a value that rules out the smallest number of values in
variables connected to the current variable through constraints.

CSP's that work with iterative improvement are often called "heuristic repair" methods, because they repair inconsistencies in the current configuration. Tree-structured CSPs can be solved in linear time.
