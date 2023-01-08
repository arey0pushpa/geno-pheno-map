# geno-pheno-map

A genotype to phenotype map is a tool that helps scientists understand how an organism's genetics lead to its physical and behavioral traits. This knowledge can be used for medical and agricultural research.

The question of how genotypic changes and variation affect phenotypes, upon which
evolutionary selection acts, is of fundamental importance in biology. One way to address
this is to talk of a map that links genotypes to phenotypes and there is a wide range of
ways to define such a genotype to phenotype map. Perhaps the more traditional way
is to address a biological model system which forms a part of the entire organism, such
as how RNA or DNA sequences determine molecular function. These can be one
layered or more complex, taking into account biophysically realistic models. There also
exist incredibly detailed computational artificial life models such as toyLIFE and other
‘digital organisms’.

## The Model

Here we attempt a more abstract definition of a genotype to phenotype map in terms
of binary variables related through gates. Our map has n nodes at each layer, and L
layers. 
Each node can take on binary values. At the lowest layer, these nodes represent
genotypes. The top layer has information about the phenotype. 
We define P number of phenotypic variables that each are a sum of n/P nodes of the top layer.
The interactions of each layer of a map are defined randomly according to the following rules: 

1) Each node has three inputs from the layer below. The same input may be an input to multiple
nodes in the layer above, and some may not be an input to any layer. 
2) The value taken on by each node is decided by a majority-inverter graph of its three inputs. A certain
proportion, q, of edges in all graphs are negated. These are chosen randomly for each map.

Thus, the genotype deterministically fixes the phenotype for each map structure given
by parameters n, L and q.
