
A small utility to convert Unix `lsof` output to a graph showing FIFO and UNIX interprocess communication.

Generate graph:

````shell
sudo lsof -n -F | ./lsofgraph | dot -Tjpg > /tmp/a.jpg
````

or add `unflatten` to the chain for a better layout:

````shell
sudo lsof -n -F | ./lsofgraph | unflatten -l 1 -c 6 | dot -T jpg > /tmp/a.jpg
````

It seems that Lua was an unfortunate choice, since people keep sending me links to ports in other languages. If you also hate Lua, raise your hand and check the Python port at https://github.com/akme/lsofgraph-python or the Perl port at https://github.com/tehmoth/lsofgraph.

![example output](/example.jpg)



