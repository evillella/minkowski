# Minkowski Weights
## Short summary
[Sage](http://www.sagemath.org) class to compute products of [Minkowski weights](https://arxiv.org/abs/alg-geom/9403002). See the [pull request](https://trac.sagemath.org/ticket/28262) for the current status and more details. I wrote this as part of my [PhD thesis](http://d-scholarship.pitt.edu/37392/). I want to add a couple more features, then the package will be ready for contribution!!

## Longer version:
[Sage](http://www.sagemath.org) is Python-based open source math software with support for many kinds of mathematical objects and operations.

### Minkowski weights and fans
This class computes products of Minkowski weights. A Minkowski weight is a function on a fan. A fan is a collection of cones such that the intersection of any pair of cones (if non-empty) is in the collection, and any face of a cone in the collection is also in the collection. A simple example is a collection of rays from the origin in 2D space. A weight is then an assigment of a number to each cone in the fan subject to a balancing condition. In 2-dimensions, the balancing condition just requires that the weighted sum of ray generators (long story, usually just the first point on the ray where all coordinates are integers) is zero. For higher dimensional cones or fans, you have a balancing condition for each subcone. This is all accounted for in the code.

Given a fan, my code: 
* checks whether a function on that fan is balanced
* determines a basis for the vector space of weights on that fan

For mathematical reasons, people care about the dimensions of these vector spaces.

### Products of weights
By [mathematics](https://arxiv.org/abs/alg-geom/9403002), it has beens shown that there is a product structure on the set of Minkowski weights. I lied a little bit above - a weight is a function on cones of just a single dimension. If the given fan contains cones of dimensions 0, 1, 2, 3, then a weight would be a functions on only rays (dimension 1), for example. 
