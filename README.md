
Generate graph:

````
sudo lsof -n -F | ./lsofgraph | dot -Tjpg > /tmp/a.jpg
````

or add 'unflatte' to the chain for a better layout:

````
sudo lsof -n -F | ./lsofgraph | unflatten -l 1 -c 6 | dot -T jpg > /tmp/a.jpg
````


