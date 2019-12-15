" Talk on trust

" Talk on belief


# A game theory framework 

Author : Benjamin Miquel

## Introduction

Game theory modeling currently revolves around writing models for specific use
cases, this paper will attempt creating a unifying framework, on which the core
principles of game theory are kept and in which the data will express the
situation to model.

Such a framework will inherently rely on game theory methods, and for that
reason, this paper will explore the different concepts that already exists, and
add, change or delete them from the framework.

## Open graph

This framework relies on a graph to represents possible solutions.  The graph
may only contain a single node, but may also contain multiple unconnected
sub-graphs. The particularity of this graph is that it is dynamically generated,
hence why it is called an open graph.

In this context, an open graph is only a serie of nodes with _conditionals
functions_ that will allows each nodes to be reached.

_Conditional functions_ are able to access variables within the project scope.
The project scope is named the _World_, all variables are contained within,
every function has access to the _World_ variables.

### Usable world variable

Nodes represent problems, a problem is a situation that can be solved through
_players'_ actions. For example a situation in which there is a buyer and a
seller, where two or more parties are trying to reach a solution, one to buy an
object and the other to sell it.

Nodes' solutions will set some variables in the World. When a solution is
reached, some variables in the world will change to take the change into
account.

### Programmed variables

Programmed variables also live within the world, they represents variables
controlled by the _experiment_, these are read only variables. An example of
such variable would be the _time of the day_, they can only be modified by the
experiment itself, an example of these variables, could be _price of the oil
barrel_, or the _weather_.

These aren't easy to implement, and will be explored in more details in the
_experiment_ section.

### Variable scope

All variables are accessible within the world, though it is important to clarify
that the players themselves may not have access to all the variables from the
World or have to access them through proxies. Example, the weather in Manilla is
sunny, but from a player based in London this information is only accessible
using proxies like, the weather channel. This is a system that allows players to
_lie_, when used as proxies.

## Utility functions

Utility functions have been a tool in game theory since its inception, they
reprensent the players' incentives. These utility functions may take any
variables present in the world and create a score specific to the player in
order for the player to determine their most favorable outcome.

