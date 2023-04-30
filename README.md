Download Link: https://assignmentchef.com/product/solved-cs218-project-1-network-analysis-using-graphs
<br>
<h1><em>Network Analysis using Graphs </em></h1>

<h2>First things first</h2>

Before starting the project (or reading this statement) you should shout out the following three times! <strong>“I will learn something new and exciting in this project” </strong>

<h2>Overview</h2>

There are three datasets given with this project statement. You are required to complete the tasks, given below, for any one of the datasets. At the maximum, you can try any two of the three datasets for more understanding on how graphs help in investigating hidden patterns in the data (you can read it as, “for bonus marks”). You should first try to complete all the tasks on the smallest dataset and then use the same code for the others.

You are also required to submit a one-page report about your understanding of the dataset. In the report you are required to explain the patterns in the dataset as much as you can.

<strong>Note: Your program MUST present a cool menu to run the tasks one at a time or all at once. We will use this menu to test your program. If the menu is not cool/useful, then we will deduct 20 marks from the overall obtained marks. If the output is not cool/readable, we will deduct further 10 marks from the overall obtained marks.  </strong>

<strong>Grading will be done individually after a demo. If a member is unable to explain the working/demo of the project, he/she will be given the minimum (say zero) marks in the project while others will get according to their understanding.</strong>

<h2>Datasets</h2>

<h3>1. General Relativity and Quantum Cosmology collaboration network Dataset Description</h3>

Arxiv GR-QC (General Relativity and Quantum Cosmology) collaboration network is from the e-print arXiv <a href="https://arxiv.org/archive/gr-qc">(</a><a href="https://arxiv.org/archive/gr-qc">https://arxiv.org/archive/gr</a><a href="https://arxiv.org/archive/gr-qc">–</a><a href="https://arxiv.org/archive/gr-qc">qc</a><a href="https://arxiv.org/archive/gr-qc">)</a> and covers scientific collaborations between authors papers submitted to General Relativity and Quantum Cosmology category. If an author i co-authored a paper with author j, the graph contains a undirected edge from i to j. If the paper is co-authored by k authors this generates a completely connected (sub)graph on k nodes.

The data covers papers in the period from January 1993 to April 2003 (124 months). It begins within a few months of the inception of the arXiv, and thus represents essentially the complete history of its GR-QC section.

<h3>2. Astro Physics collaboration network Dataset Description</h3>

Arxiv     ASTRO-PH         (Astro   Physics)            collaboration    network            is          from     the       e-print arXiv <a href="https://arxiv.org/archive/astro-ph">(</a><a href="https://arxiv.org/archive/astro-ph">https://arxiv.org/archive/astro</a><a href="https://arxiv.org/archive/astro-ph">–</a><a href="https://arxiv.org/archive/astro-ph">ph</a><a href="https://arxiv.org/archive/astro-ph">)</a> and covers scientific collaborations between authors papers submitted to Astro Physics category. If an author i co-authored a paper with author j, the graph contains a undirected edge from i to j. If the paper is co-authored by k authors this generates a completely connected (sub)graph on k nodes.

The data covers papers in the period from January 1993 to April 2003 (124 months). It begins within a few months of the inception of the arXiv, and thus represents essentially the complete history of its ASTROPH section.

<h3>3. Amazon product co-purchasing network and ground-truth communities Dataset Description</h3>

Data was collected by crawling Amazon website. It is based on <em>Customers Who Bought This Item Also Bought </em>(explained here: <a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">https://davidgaughran.com/also</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">–</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">boughts</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">–</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">amazon</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">–</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">recommendations/</a><a href="https://davidgaughran.com/also-boughts-amazon-recommendations/">)</a> feature of the Amazon website. If a product<em> i</em> is frequently co-purchased with product <em>j</em>, the graph contains an undirected edge from <em>i</em> to <em>j</em>. Each product category provided by Amazon defines each ground-truth community.

We regard each connected component in a product category as a separate ground-truth community. We remove the ground-truth communities which have less than 3 nodes.

<h2>Tasks</h2>

<h3>First Set of Tasks – Graph Stats</h3>

<ol>

 <li>Display the number of nodes (5 marks)</li>

 <li>Display the number of edges (5 marks)</li>

 <li>Display the number of source nodes (5 marks)</li>

 <li>Display the number of sink nodes (5 marks)</li>

 <li>Display the number of isolated nodes (5 marks)</li>

 <li>Display the number of bridge edges (15 marks)</li>

 <li>Display the number of articulation nodes (15 marks)</li>

 <li>Display the shortest path length distribution (20 marks)</li>

 <li>Display the diameter of the graph (5 marks)</li>

</ol>

<h3>Second Set of Tasks – Degree Distributions</h3>

<ol start="10">

 <li>Display the in-degree distribution in the form of a table (10 marks)</li>

 <li>Display the out-degree distribution in the form of a table (10 marks)</li>

</ol>

<h3>Third Set of Tasks – Connected Components</h3>

For the original graph:

<ol start="12">

 <li>Display the size of the largest strongly connected component (SCC) (25 marks)</li>

 <li>Display the size distribution of all SCCs (10 marks)</li>

</ol>

Considering the graph as an undirected graph:

<ol start="14">

 <li>Display the size of the largest weakly connected component (WCC) (25 marks)</li>

 <li>Display the size distribution of all WCCs (10 marks)</li>

</ol>

<h2>Algorithms</h2>

You will need the following algorithms for the third set of tasks.

<h3>Breadth-First Search (BFS) Algorithm</h3>

The BFS algorithm (Algorithm 1) takes as input a graph <em>G(V, E) </em>and a source vertex <em>s</em>. The algorithm returns the set of vertices that the source vertex has a path to.




<h3>Strongly Connected Components (SCC) Algorithm</h3>

The SCC algorithm (Algorithm 4) takes a graph <em>G(V, E) </em>as input and returns a list of all the SCCs in this graph as output. The SCC of <em>G </em>is computed using Eq. 1.21. The function <em>unique </em>returns a list of all the distinct elements in the input list. For instance, <em>unique</em>([1,2,1,3,2,2]) will return [1,2,3].

<h3>Weakly Connected Components (WCC) Algorithm</h3>

The WCC algorithm (Algorithm 5) computes the list of all WCCs given a graph G(V, E) as input.




<h2>Definitions</h2>

<strong>Source Vertex:</strong> A vertex with zero in-degree is called a source vertex

<strong>Sink Vertex:</strong> A vertex with zero outdegree is called a sink vertex

<strong>Isolated Vertex:</strong> A vertex with in-degree and out-degree both equal to zero is called an isolated vertex.

<strong>Degree Distribution:</strong> The degree distribution of a graph G(V, E), denoted by P(k), is defined as the probability that a random chosen vertex has degree k. If |V|k denotes the number of vertices with degree

k,




<strong>Bridge Edge:</strong> A bridge edge is an edge whose removal disconnects the graph.

<strong>Articulation Vertex:</strong> An articulation vertex is defined as a vertex which when deleted renders the graph a disconnected one.

<strong>Diameter:</strong> The diameter of a graph is the maximum of the distances between all pairs of vertices in this graph. While computing the diameter of a graph, all infinite distances are disregarded