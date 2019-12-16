" Talk on trust

" Talk on belief


# A game theory framework 

Author : Benjamin Miquel

## Introduction

Game theory modeling currently revolves around writing models for specific use
cases, this paper will attempt the creation of an unifying framework, on which the core
principles of game theory are kept and in which the data will express a
situation to model.

Such a framework will inherently rely on game theory methods, and for that
reason, this paper will explore the different concepts that already exists, and
add, change or remove them from them framework.

## Open graph

This framework relies on a graph to represents possible solutions. The graph
may only contain a single node, or may also contain multiple unconnected
sub-graphs. The particularity of this graph is that it is dynamically generated,
hence why it is called an open graph.

In this context, an open graph is a serie of nodes with _conditionals
functions_ that will allows each node to be reached.

_Conditional functions_ are able to access variables within the project scope.
The project scope is named the _World_, all variables are contained within,
every function has access to the _World_ variables.

## Node outcomes 

A node represents a problem which can be solved through _players'_ actions. For
example, a buyer and a seller have to agree on the price of a car. Outcomes
could have the car priced at different values but also the car not being sold at
all. 

Nodes' solutions will set variables in the World. When a solution is reached,
variables in the world will change to take the change into account.

## Programmed variables

Programmed variables also live within the world, they represents variables
controlled by the _experiment_, these are read only variables. An example of
such variable would be the _time of the day_, they can only be modified by the
experiment itself, an example of these variables, could be _price of the oil
barrel_, or the _weather_, they could be static, or change during the experiment.

These aren't easy to implement, and will be explored in more details in the
_experiment_ section.

## Variable scope

All variables are accessible within the world, though it is important to clarify
that the players themselves may not have access to all the variables from the
World or have to access them through proxies. Example, the weather in Manilla is
sunny, but from a player based in London this information is only accessible
using proxies like, the weather channel. This is a system that allows players to
_lie_, when used as proxies.

## Utility functions

Utility functions have been a tool in game theory since its inception, they
reprensent the players' incentives. These utility functions take any
variables present in the world and create a score specific to the player in
order for the player to determine their most favorable outcome. 

## Experiment

An _experiment_ is what is being run when solving the graph, it takes the graph,
and the initial values of the variables. These variables can be set to change on
certain condition, or when the the graph is _stuck_ which would suggest that
there is nothing to do anymore.

For example, a node could await a certain time to pass before being activated,
or re-activated.

## Computation of outcomes

Players will always do what is best for them, and follow their incentives, their
are often constrained by agreement or contracts. These contracts are virtual
nodes, set in the future. For example, player Hungry orders food to player
Restorant, and enters creates a contract in which Players Hungry agrees to pay
after the food is eaten. This contract can be defaulted, player Hungry could run
away, or refuse to pay, then player Restorant would need to decide to persue or
not Hungry.



