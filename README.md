
## Dimensionality Reduction 

The goal of these exersizes is to get introduced to dimensionality reduction techniques and gain some intuition behind PCA and SVD. 


### Curse of Dimensionality

> The curse of dimensionality refers to various phenomena that arise when analyzing and organizing data in high-dimensional spaces (often with hundreds or thousands of dimensions) that do not occur in low-dimensional settings such as the three-dimensional physical space of everyday experience.

The curse of dimensionality is a phenomenon that any model/technique which involves a distance metric suffers from.  Due to the number of features, even the closest data points seem very far away.  A simple way to see this is with Euclidean distance:

![](http://upload.wikimedia.org/math/a/0/5/a056c1b3e4b1c72be81acf62b9e574ca.png)

As __n__ grows, the distance grows without bounds.

Even models that do not explicitly use a distance metric can be affected by a high number of dimensions.  A rough heuristic for a model to be effective is that you need the distance between points to be less than some value __d__.  For a single dimension (unit-length) this usually requires on average __1/d__ points.  If you have __p__ dimensions the number of data points you need scales as __1/d^p__.
