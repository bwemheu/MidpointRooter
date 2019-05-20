# MidpointRooter
Midpoint-rooting of large phylogenetic trees

Most midpoint-root functions convert trees to cophentic distances to find the pair with the highest distance. However, large trees and the deduced distance matrix need heaps of memory. This package contains the function "midpoint.root2" deduced from the midpoint.root function in phytools. It uses a pairwise-approach to detect this pair. Slow but does the job.

## Instructions
1) Install phytools via CRAN
2) Download and install the MidpointRooter package (https://github.com/bwemheu/MidpointRooter/raw/master/MidpointRooter_0.1.0.tar.gz)
3) Use the midpoint.root2 function to root a tree

In R:
```
library(phytools)
library(MidpointRooter)
tree_unrooted = read.tree("treeFile.phy")
tree_rooted = midpoint.root2(tree = tree_unrooted)
write.tree(phy = tree_rooted, file = "treeFile_rooted.phy")
```
