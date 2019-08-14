
Dynamic Graph
============

Dynamic Graph is a simple Python module for generating a graph with its edge degrees and sizes of connected components following a power law
distribution. Its complexity is O(N) strictly.

[A Live DEMO](https://dynamicgraph.herokuapp.com)

**Prerequisites:** 

- [Python 3](https://www.python.org/),  [scipy](https://www.scipy.org/), [numpy](http://www.numpy.org/),
[collections](https://docs.python.org/2/library/collections.html), [random](https://docs.python.org/3/library/random.html)

Motivation
==========

The scale of big data being collected and stored is rapidly expanding. Graph analytics aims to extract relations from this huge amount of data. In this project, I'm generating a random graph in a complexity of O(n) to support billions of nodes and relations in a dynamic way. Many mega networks follow a power law distribution, also called a 80-20 rule, like street network in which national highways connect most of the others. Another example is airport terminals and the HUBs like Heathrow and Chicago contribute to major traffics. This project seeks for the answers to some simple and enlightening questions, if one HUB stopped working, how great the impact will be brought to the entire network. A big graph takes time for indexing the nodes and relations as well as searching in a recursive or none-recursive way all visited nodes. What if new nodes family added that have to reconstruct the whole network? Throughout this journey, I proposed a way using barabási–albert model to generate the graph dynamically and also monitored changes in its capacity to deal with billions of nodes and relations without need to reconstruct the entire network, in case that a single node is added or removed.

Tests
----------

I include test program to troubleshoot the use of the library.  It's a simple command line process to run the test.

    python test_graph.py
    
Output:

    ----------------------------------------------------------------------
    The size of the main frame is 523
    Time used to add new nodes dynamically  0:00:04.091755
    The size of the main frame is 497
    Time used to delete nodes dynamically  0:00:01.972822
    The size of the main frame is 581
    Time used to add new nodes dynamically  0:00:03.359419
    The size of the main frame is 540
    Time used to delete nodes dynamically  0:00:01.879742

Available Classes
-----------------

There are two classes in `Dynamic Graph`:

- `GraphNode` - Returns a class of Node in the graph.
- `ProbGraph` - Returns a class of processed graph following a power-law rule of edge degrees for every node and size of components based on the node numbers, max edge numbers and special curves pattern.

LICENSE
=======

Dynamic Graph is licensed to you under MIT.X11:

Copyright (c) 2019 Chao (Chase) Xu

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
