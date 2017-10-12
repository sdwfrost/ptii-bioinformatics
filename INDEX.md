# Part II Bioinformatics notes

This page is for answering questions related to the course. Please post additional questions as issues [here](https://github.com/sdwfrost/ptii-bioinformatics/issues), or email me (sdf22) if you need help.

## Some problems to think about

### Alignment

1. Researchers often sequence only part of the genome, such that there are terminal 'gaps' in the alignment. How would you deal with these?
2. Sequences may code a protein. Most often, sequences are translated into amino acids before alignment. How would you align sequences in nucleotide space?
3. In addition to A,C,G,T, there are also [symbols for ambiguous nucleotides](https://en.wikipedia.org/wiki/Nucleic_acid_notation#.3Cspan_class.3D.22searchmatch.22.3EIUPAC.3C.2Fspan.3E_notation). How would you deal with these?
4. Progressive methods for multiple sequence alignment require us to identify 'similar' sequences. How can we do this without an alignment in the first place?

## Questions

### Alignment

1. Couldn't we just use a shortest path algorithm in place of the longest path algorithms, by transforming the graph?

If $G$ is the weighted graph, you could take the shortest path in $-G$. As the weights are negative, you would have to use an algorithm such as the [Bellman-Ford](https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford_algorithm) algorithm; as the alignment graph is a DAG, we don't have to worry about negative cycles. However, the runtime of the Bellman-Ford algorithm is $O(VE)$, whereas the algorithms in class are $O(V+E)$. In general, there is the problem of obtaining a topological sorting, but this is straightforward in the case of the alignment graph.

## Typos
