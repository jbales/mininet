#####  Simple Tree Topology with Fanout 2 (Professor: Nick Feamster)
source : https://d396qusza40orc.cloudfront.net/sdn/srcs/programming-assignment-2.zip

<j>Data center networks typically have a tree-like topology. End-hosts connect to top-of-rack switches, which form the leaves (edges) of the tree; one or more core switches form the root; and one or more layers of aggregation switches form the middle of the tree. In a basic tree topology, each switch (except the core switch) has a single parent switch. Additional switches
and links may be added to construct more complex tree topologies (e.g., fat tree) in an effort to improve fault tolerance or increase inter-rack bandwidth. In this assignment, your task is to create a simple tree topology. You will assume each level i.e., core, aggregation, edge and host to be composed of a single layer of switches/hosts with a configurable fanout value (k). For example, a simple tree network having a single layer per each level and a fanout of 2 looks like:</j>

<img src="https://github.com/syaifulahdan/mininet/blob/master/image/Screenshot%20from%202016-04-02%2002:44:01.png" align="center" title="syaifulahdan/mininet" />

download consists of two files:


- <a href="https://github.com/syaifulahdan/mininet/blob/master/py-custop_tree_topology_with_Fanout2-custom_topo.py">custom-topo.py:</a> a sekleton class which you will update with the logic for creating the datacenter topology described above.
- <a href="https://github.com/syaifulahdan/mininet/blob/master/py-custop_tree_topology_with_Fanout2-submit.py">submit.py:</a>  used to submit your code and output to the course servers for grading. You don’t have to do any modifications in here.

##### CustomTopo.py
The skeleton class takes following arguments as input:
- linkopts1: for specifying performance parameters for the links between core and aggregation switches.
- linkopts2: for specifying performance parameters for the links between aggregation and edge switches.
- linkopts3: for specifying performance parameters for the links between edge switches and host.
- Fanout: to specify fanout value i.e., number of childs per node.