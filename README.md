# Reference implementation of generalized face-spiral nomenclature for polyhedral graphs

This software implements the methods described in our research paper
[Naming Polyhedra by General Face-Spirals](https://doi.org/10.1080/1536383X.2017.1388231).

Specifically, we provide a method for compact, canonical naming of all
[polyhedral graphs](https://en.wikipedia.org/wiki/Polyhedral_graph)
(the 3-connected planar graphs), and polyhedral molecules, i.e.,
molecules whose bond structures are polyhedral graphs.

This is done through a generalization of <em>face spirals</em>,
introduced by Manolopoulos for fullerenes in the 1990's, to encode any
polyhedral graph up to isomorphism. The spiral code is found by
unraveling the polyhedral graph face-by-face, like peeling an orange,
while writing down the face sizes; and to construct the polyhedron
from the spiral, one rolls up the “orange peel” of face sizs. These
intuitive operations can be formulated as simple graph constructions,
yielding fast, and robust computer algorithms.

Our scheme is compatible with Manolopoulos' classical face spiral
scheme whenever the classical scheme succeeds. We also provide a
nomenclature for all polyhedral molecules that yields canonical,
unambiguous, unique, and concise names.

Especially compact names are given to <em>fullerenes</em> (cubic
polyhedral graphs with only hexagon and pentagon faces, which require
only around 12 numbers to represent) and <em>fulleroids</em> (cubic
polyhedral graphs with any face size allowed), for which most classes
have similar compact representations.

## Source code overview

The software provided here is in the form of two small C++ libraries,
which can easily be incorporated into your own software, together with
command-line utilities in the directory `programs`. The
bare-bones functionality is:

1. Given a 3-connected planar graph, compute its generalized spiral
   representation and canonical name.
2. Given a spiral code string, compute the polyhedral graph.

The code for this is given in the `spiral-clean/` directory. A much
more versatile library for working with polyhedral graphs, cubic
graphs, and triangulations, is found under `libgraph/`. This is
our graph library from our Fullerene program (http://tinyurl.com/fullerenes),
and includes many other operations than spiral names.

## Citing

You are encouraged to incorporate this reference implementation in
your own software (under the BSD license), but we ask that you write
us an email if you do. You are also welcome to write us if you are
interested in using it but encounter obstacles doing so. 
<pre>
James Avery (avery at nbi.ku.dk)
Lukas Wirz  (email in AUTHORS file)
Peter Schwerdtfeger (email in AUTHORS file)
</pre>

In addition, if you use this in academic work, please cite the
following paper:

<table>
<tr>
<td>
<pre>
@article{SpiralCodes2017,
  author = {Lukas N. Wirz and Peter Schwerdtfeger
            and James E. Avery},
  title = {Naming Polyhedra by General Face-Spirals:
           Theory and Applications to Fullerenes and
           other Polyhedral Molecules},
  journal = {Fullerenes, Nanotubes and Carbon Nanostructures},
  volume = {0},
  number = {ja},
  pages = {0-0},
  year  = {2017},
  publisher = {Taylor & Francis},
  doi = {10.1080/1536383X.2017.1388231}
}
</pre>
</td>
<td>
<a href="https://doi.org/10.1080/1536383X.2017.1388231">
<img src="http://www.nbi.dk/~avery/Polyhedra/images/gs_paper-spiralpage-400px.png" width="300px"/>
</a>
</td>
</tr>
</table>

If you use the full `libgraph` library, we ask that you also cite our Fullerene project, which it is extracted from.
The associated papers are

<table>
<tr>
<td>
<pre>
@article {ProgramFullerenes2013,
  author = {Schwerdtfeger, Peter and Wirz, Lukas and Avery, James},
  title = {Program Fullerene: A software package for constructing
           and analyzing structures of regular fullerenes},
  journal = {Journal of Computational Chemistry},
  volume = {34},
  number = {17},
  issn = {1096-987X},
  url = {http://dx.doi.org/10.1002/jcc.23278},
  doi = {10.1002/jcc.23278},
  pages = {1508--1526},
  year = {2013}
}
</pre>
</td>
<td>
<a href="http://onlinelibrary.wiley.com/doi/10.1002/jcc.23278/abstract"><img src="http://onlinelibrary.wiley.com/store/10.1002/jcc.23343/asset/image_m/jcc23343-fig-0001-m.png?v=1&s=c563bd44689bbc8815ce750658ba6fda2b8e51e5" width="300px" /></a>
</td>
</tr>
</table>
and
<table>
<tr>
<td>
<pre>
﻿@article {FullereneTopology2015,
  author = {Schwerdtfeger, Peter and Wirz, Lukas N and Avery, James},
  title = {The topology of fullerenes},
  journal = {Wiley Interdisciplinary Reviews:
             Computational Molecular Science},
  volume = {5},
  number = {1},
  publisher = {Wiley Periodicals, Inc.},
  issn = {1759-0884},
  url = {http://dx.doi.org/10.1002/wcms.1207},
  doi = {10.1002/wcms.1207},
  pages = {96--145},
  year = {2015},
}
</pre>
</td>
<td>
<a href="http://wires.wiley.com/WileyCDA/WiresArticle/wisId-WCMS1207.html"><img src="http://www.nbi.dk/~avery/Polyhedra/images/WIREpaper-transform-page-400px.png" width="300px"></a>
</td>
</tr>
</table>

<table>
<tr><td>
<a href="http://onlinelibrary.wiley.com/doi/10.1002/jcc.23343/full"><img src="http://onlinelibrary.wiley.com/store/10.1002/jcc.23343/asset/image_m/jcc23343-fig-0001-m.png?v=1&s=c563bd44689bbc8815ce750658ba6fda2b8e51e5" width="300px" /></a>
</td><td>
<a href="http://wires.wiley.com/WileyCDA/WiresArticle/wisId-WCMS1207.html">
<img src="http://pubs.acs.org/appl/literatum/publisher/achs/journals/content/jcisd8/2014/jcisd8.2014.54.issue-1/jcisd8.2014.54.issue-1/production/jcisd8.2014.54.issue-1.largecover.jpg"/></a>
</td>
<td>
<a href="http://wires.wiley.com/WileyCDA/WiresArticle/wisId-WCMS1207.html">
<img src="http://www.nbi.dk/~avery/Polyhedra/images/WIREpaper-transform-page-400px.png" width="300px">
</a>
</td>
<td>
<a href="https://doi.org/10.1080/1536383X.2017.1388231">
<img src="http://www.nbi.dk/~avery/Polyhedra/images/gs_paper-spiralpage-400px.png" width="300px"/>
</a>
</td>
</tr>
</table>
