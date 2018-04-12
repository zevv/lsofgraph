
A small utility to convert Unix `lsof` output to a graph showing FIFO and UNIX interprocess communication.

Generate graph:

````shell
sudo lsof -n -F | ./lsofgraph | dot -Tjpg > /tmp/a.jpg
````

or add `unflatten` to the chain for a better layout:

````shell
sudo lsof -n -F | ./lsofgraph | unflatten -l 1 -c 6 | dot -T jpg > /tmp/a.jpg
````

In case you are not happy using Lua, there is also a Python port of this script available at
https://github.com/akme/lsofgraph-python

![example output](/example.jpg)



