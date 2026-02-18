# Artificial Intelligence – Introduction

Artificial Intelligence (AI) is a branch of computer science that builds systems capable of tasks requiring human intelligence, such as learning, reasoning, and decision-making.

## Definition
AI is the science and engineering of creating intelligent machines and software that can perceive, learn, and act.

## Key Characteristics
- Learns from data
- Reasons and makes decisions
- Solves problems
- Adapts to new situations

## Common Applications
- Virtual assistants (Siri, Alexa)
- Medical diagnosis support
- Self-driving vehicles
- Recommendation systems (Netflix, YouTube)

## Goals of AI
- Simulate intelligent behavior
- Learn from experience
- Solve complex problems efficiently
- Support human decision-making
- Improve automation and productivity

## Types of AI
### Weak AI (Narrow AI)
Built for specific tasks only.

Examples: chatbots, voice assistants, recommendation systems.

### Strong AI (General AI)
Would perform any intellectual task like humans.

Status: theoretical, not yet achieved.

## AI vs Human Intelligence
- AI: fast computation, data-driven decisions
- Humans: creativity, emotions, contextual understanding

## Advantages of AI
- Reduces human effort
- Improves speed and accuracy
- Works continuously without fatigue
- Helps solve complex tasks

## Disadvantages of AI
- High development cost
- Limited creativity and emotions
- Dependence on machines
- Potential job displacement

## Intelligent Agents
An intelligent agent perceives its environment (through sensors) and acts on it (through actuators) to achieve goals.

### Components
- Sensors
- Actuators
- Agent program
- Environment

### Types
- Simple reflex agent
- Model-based agent
- Goal-based agent
- Utility-based agent
- Learning agent

## AI Problem Solving
AI problem solving means finding a sequence of actions from an initial state to a goal state.

### Basic Steps
1. Define the problem
2. Identify initial state
3. Define goal state
4. List possible actions
5. Apply search strategy

### Role of Heuristics
A heuristic is a rule-of-thumb that helps reach solutions faster by reducing the search space.

## Generate and Test
Generate possible solutions and test them one by one until a valid solution is found.

### Pros
- Simple to understand
- Useful for small search spaces

### Cons
- Slow for large problems
- Not always optimal

## Hill Climbing
A heuristic method that repeatedly moves to a better neighboring state.

### Limitation
Can get stuck in local maxima, plateaus, or ridges.

## Search Strategies

### Uninformed (Blind) Search
- **BFS**: level by level, complete and optimal (equal costs)
- **DFS**: deep first, not always optimal
- **Uniform Cost Search**: expands lowest path cost, optimal

### Informed (Heuristic) Search
Uses heuristic function $h(n)$ to estimate distance to goal.

- **Best-First Search**: $f(n)=h(n)$
- **A\***: $f(n)=g(n)+h(n)$

Where:
- $g(n)$ = cost from start to current node
- $h(n)$ = estimated cost from current node to goal

### Admissible Heuristic
A heuristic is admissible if it never overestimates true cost.

Example: straight-line distance in maps.

## Quick Comparison
| Algorithm | Uses Heuristic | Optimal | Complete |
|---|---|---|---|
| BFS | No | Yes | Yes |
| DFS | No | No | No |
| Best-First | Yes | No | No |
| A* | Yes | Yes | Yes |

## Conclusion
Search is central to AI problem solving, and heuristic methods like A* improve efficiency in real-world tasks such as route planning and robotics.
Add this **after Search Strategies**:

## Knowledge Representation and Reasoning (KRR)

Knowledge Representation and Reasoning is a core area of AI that focuses on storing knowledge in a form that machines can use to solve problems and make decisions.

### Why KRR is Needed
- Helps AI understand facts about the world
- Supports logical decision-making
- Improves problem solving in complex situations
- Enables explanation of conclusions

### Types of Knowledge in AI
- **Declarative knowledge:** facts (what is true)
- **Procedural knowledge:** steps or methods (how to do)
- **Heuristic knowledge:** rules of thumb
- **Meta-knowledge:** knowledge about other knowledge

### Common Knowledge Representation Techniques
- **Logic-based representation** (Propositional and Predicate Logic)
- **Semantic Networks** (nodes and relationships)
- **Frames** (structured object-like records)
- **Production Rules** (`IF condition THEN action`)

### Reasoning in AI
Reasoning is the process of deriving new information from known facts.

#### 1) Deductive Reasoning
- Moves from general rule to specific conclusion
- If premises are true, conclusion is guaranteed true

#### 2) Inductive Reasoning
- Moves from specific observations to general rule
- Conclusion is probable, not guaranteed

#### 3) Abductive Reasoning
- Finds the most likely explanation for observations

### Inference
Inference is applying rules to known facts to get new facts.  
Example rule: `IF human(X) THEN mortal(X)`.

### Applications of KRR
- Expert systems
- Medical diagnosis
- Legal advisory systems
- Chatbots and virtual assistants
- Planning and decision support systems

### Limitations of KRR
- Difficult to represent real-world uncertainty
- Large knowledge bases are hard to maintain
- Ambiguity in natural language

## Short Conclusion
KRR gives AI the ability to represent knowledge and reason logically, making systems more intelligent and useful in real-world decision-making.

If you want, I can give the next topic in the same flow: **Expert Systems** (architecture, components, advantages, limitations).
## Topic: A* Search Algorithm

### Introduction
A* (A-Star) is an informed search algorithm that finds the shortest path between start and goal nodes. 
It combines the advantages of Uniform Cost Search and Greedy Best First Search.

### Evaluation Function
A* uses the function:

f(n) = g(n) + h(n)

Where:
g(n) = actual cost from start node to current node  
h(n) = heuristic estimate from current node to goal  
f(n) = total estimated cost

### Working Principle
1. Start from initial node.
2. Calculate f(n) for all neighbor nodes.
3. Select the node with lowest f(n).
4. Repeat until goal is reached.

### Properties
- Complete: Yes (if heuristic is admissible)
- Optimal: Yes (if heuristic is admissible)
- Efficient compared to uninformed search

### Example
If:
g(n) = 5
h(n) = 3
Then:
f(n) = 5 + 3 = 8

The algorithm chooses node with minimum f(n).

### Advantages
- Faster than uninformed search
- Guarantees shortest path (with admissible heuristic)

### Disadvantages
- High memory usage
- Performance depends on heuristic quality

### Applications
- GPS Navigation
- Robotics path planning
- Game AI
- Network routing
