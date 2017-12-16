# Reference implementation of generalized face-spiral nomenclature for polyhedral graphs

This software implements the methods described in our research paper
[Naming Polyhedra by General Face-Spirals](https://doi.org/10.1080/1536383X.2017.1388231).

Specifically, we provide a method for compact, canonical naming of all
[polyhedral graphs](https://en.wikipedia.org/wiki/Polyhedral_graph)
(the 3-connected planar graphs), and polyhedral molecules, i.e.,
molecules whose bond structures are polyhedral graphs.

This is done through a generalization of <em>face spirals</em>,
introduced by Manolopoulos for fullerenes in the 1990's, to encode any
polyhedral graph up to isomorphism. This scheme is compatible with
Manolopoulos' classical face spiral scheme whenever the classical
scheme succeeds. We also provide a nomenclature for all polyhedral
molecules that yields canonical, unambiguous, unique, and concise
names.

Especially compact names are given to <em>fullerenes</em> (cubic
polyhedral graphs with only hexagon and pentagon faces) and
<em>fulleroids</em> (cubic polyhedral graphs with any face size
allowed).

The software provided here is in the form of a small C++ library,
which can easily be incorporated into your own software. 

## Citing

You are encouraged to incorporate this reference implementation in
your own software (under the BSD license), but we ask that you write
us an email if you do. You are also welcome to write us if you are
interested in using it but encounter obstacles doing so.

In addition, if you use this in academic work, please cite the
following paper:

```
@article{spiral-codes2017,
	author = {Lukas N. Wirz and Peter Schwerdtfeger and James E. Avery},
	title = {Naming Polyhedra by General Face-Spirals -- Theory and Applications to Fullerenes and other Polyhedral Molecules},
	journal = {Fullerenes, Nanotubes and Carbon Nanostructures},
	volume = {0},
	number = {ja},
	pages = {0-0},
	year  = {2017},
	publisher = {Taylor & Francis},
	doi = {10.1080/1536383X.2017.1388231}
}
```

## Source code overview

Reference implementation of generalized face spiral nomenclature for polyhedral graphs

1. libgraph/ is a nearly full version of the graph library from our
   Fullerene program (http://tinyurl.com/fullerenes), and includes many
   other operations than spiral names.
