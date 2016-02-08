
````
sudo lsof -n -F | ./lsofgraph | dot -Tjpg > /tmp/a.jpg
````

TODO: completely rework, as the current implementation is O(n²)

