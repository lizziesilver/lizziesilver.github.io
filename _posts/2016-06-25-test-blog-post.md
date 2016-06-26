---
layout: post
title: "Using Cytoscape to visualize graphs from Tetrad"
date: 2016-06-25
---

Tetrad contains an wonderful suite of causal search algorithms, but it is not so great 
for visualization. Cytoscape is free and a great tool for visualizing networks. If you 
have a medium to large graph (say, more than 50 nodes), you may find it easier to 
interpret the structure in Cytoscape. Here's how:

<ol>
<li> Save your Tetrad graph as a text file </li>
<li> The text file will look something like:
{% highlight text %}
Graph nodes:
X1 X2 X3 X4 ...

Graph edges:
1. X1 --- X2
2. X3 --> X4
...
{% endhighlight %}

Delete everything above the first edge, so your file begins with a line like "1. X1 --- X2". </li>
<li> Open Cytoscape and click on the "Import network from file" button. </li>
<li> After choosing your file, click on "Advanced options". Pick the following options: 
<ol type="a">
<li> Set the delimiter to SPACE </li>
<li> Uncheck "Variable names in first row" </li>
<li> Choose the second column to be the Source </li>
<li> Choose the third column to be the Interaction Type </li>
<li> Choose the fourth column to be the Target </li>
</ol>
</li>
<li> Click ok </li>
<li> Set the edge theme to reflect the edge endpoints in Tetrad. </li>
</ol>
