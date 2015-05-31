# 06 - Production Systems

Lesson Preview:

- Cognative Architectures
- Prodution Systems
- Chunking (Learning by)


## Cognitive Agent

It's a mapping of *precepts* to an *action*, like:

$$ f(P^*) = A $$

### Levels of Cognitive Architectures

High level to Low level, like:

- Task / Knowledge Level
  (e.g., selecting a pitch, playing baseball)
- Algorithm / Symbol Level
  (e.g., means-end analysis, semantic networks)
- Hardware / Implementation Level
  (e.g., a brain, a transitor)

Higher level architectures provide *content* to be manipulated in lower levels. Lower levels provide *architecture* for implementing what is represented in higher level. 

*Example* Smart Phone: phone allows for communication with others at long distances

### Assumptions of Cognative Architecture

- Goal Oriented: take actions in pursuit of goals
- Rich, complex environment
- Significant knowledge: leverage knowledge to achieve goals.
- Symbols and abstractions
- Flexible and function of the environment: behavior is dependant on environment
- Learning: learn through interactions

$$ Architecture + Content = Beahavior $$


Simplification: assume that Architecture is fixed, modify knowledge content to yield new behavior. 

## SOAR Architecture

A *deliberation* component, consisting of long-term memory and working memory.

- *Procedural*: How to do certain things
- *Semantic*: Generalization or models of the world
- *Episodic*: Event-based knowledge

Precepts, or short term knowledge, provides content to the procedural rules (long term knowledge), and allows for a rule to suggest an operator to be called (fired).

An *impasse* occurs when either:

1. There isn't enough short-term knowledge to 
2. There are multiple actions sugguested without any means to resolve.

An agent can invoke a *learning* process by searching episodic (instance based) memory for instances similar to current state. Outcomes of these events can allow for a *new* procedure to be created that will resolve the impasse. This is referred to as *chunking*.

