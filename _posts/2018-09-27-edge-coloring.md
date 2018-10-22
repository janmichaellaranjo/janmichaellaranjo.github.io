---
layout: post
title: "Graphs and UEFA Nations League"
subtitle: "Test"
---

<h3>Introduction</h3>
Recently I watched television and I stumbled across some sport report. Nothing special. It was about football and to be precise about the
<a href="https://www.uefa.com/uefanationsleague/">UEFA Nations League"<a/>. In short terms there exists four leagues (<i>A, B, C, D</i>) with three or four
groups consisting of national teams. <i>A</i> is the highest ranked league and <i>D</i> the lowest. Each team in a group competes against each other for
two times(First and second leg). The goal is to rise up to the highest league <i>A</i>.
A game plan of all matches was shown and this was the moment that caught my eye. There so many matches and I wondered how they could determine each match
in a group. I realized that this is a problem in graph theory. Luckily I read about approximation algorithms for the
<a href="https://en.wikipedia.org/wiki/Edhttps://en.wikipedhttps://en.wikipedge_coloring">Edge Coloring Problem</a> in the book
<a href="http://www.designofapproxalgs.com/book.pdf">The Design Of Approximation Algorithms</a> and somehow I managed to relate the problem of determining
matches in UEFA Nations League to the <i>Edge Coloring Problem</i>. So I want to dive deep more into this certain problem.

<h3>What is the Edge Coloring Problem?</h3>
So what is this problem? At first I want to give a more informal definition. Let's say you have a graph and the minimum amount of colors given. The challenge
is to color the edges of graph such that no adjacent edges have the same color. If you look each node independently, every incident edge has a different color.
So this problem is ideally suited to solve different scheduling problems.

<h3>NP-Complete</h3>
How much time does it take to find a optimal edge coloring for any graph that has any <i>chromatic index</i>? The chromatic index is the smallest amounf of
color of a edge colored graph. Unfortunately this problem is NP-complete. As a certificate you can use the graph
and colors for each edge. This can be easily checked in linear time, if the coloring is valid. Thus this problem lies in NP. Next we need to reduce a known
NP-hard problem to the <i>Edge Coloring Problem</i>. For instance we can reduce the <i>3-SAT problem</i>, which is a known NP-complete and is stated as
followed. Given a set of clauses $$C=\{C_1, C_2, C_3,...C_l\}$$ and variables $$u_1, u_2,...u_m$$, where each clause consists of 3 literals $$l_{i,1}, l_{i,2},
l_{i,3}, 1 \leq i \leq l$$, each clause is connected with an $$\land$$-operator and each literal inside a clause with a $$\vee$$-operator. Each literal is
either $$u_k$$ or $$\overline{u_k}$$ for $$1 \leq k \leq m$$. The problem is to determine, if all clauses are satisfied. A clause is satisfied, if one of the
variables in the clause is true.
<h4>Reduction</h4>
So the goal of the construction is that iff the instance of <i>3-SAT</i> is satisfied, then is the constructed graph 3 edge colorable. I will only give you an
idea how a construction from <i>3-SAT</i> to <i>Edge Coloring</i> instance could work. First we need a lemma, <b>the Parity Condition</b>, which will be used
for the reduction.
<h5>The Parity Condition</h5>
<i>Let $$G=(V,E)$$ be a cubic graph, which is 3 edge colored. Let $$V' \subseteq V$$ and $$E' \subseteq E$$  be subsets vertices and edges of $$G$$. $$E'$$
connects vertices $$V'$$ and $$V \setminus V'$$. Denote $$k_1, k_2, k_3$$ as the number of colors in $$i$$ in $$E'$$. Then the lemma exhibits</i>
<center>$$k_1 \equiv k_2 \equiv k_3  mod  2$$</center> (Holyer, 1981)
<h5>Construction Consideration</h5>
As we've already mentioned the goal is to show if a 3SAT instance C is satisfiable, the constructed graph $$G$$ is 3-edge-colorable. $$G$$ consists of
components that have certain tasks to fulfill and informations are transported through pair of edges. A pair of edges in $$G$$ represents the value $$true$$,
if the edges have the same color, else the edges have distinct colors.
//TODO:draw graph

This graph has 5 incoming edges $$\{a, b, c, d, e\}$$. If this components is 3-edge-colorable, one of the edge pairs $$(a,b)$$ or $$(c,d)$$ have the same
color and the remaining edges have different colors. This can be easily checked with the <i>Parity Condition </i>.
