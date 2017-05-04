# Decentralized indexes for public genomic data

[Luiz Carlos Irber Júnior](https://github.com/luizirber), [C. Titus Brown](https://github.com/ctb), [Tim Head](https://github.com/betatim)

- Department of Population Health and Reproduction, University of California, Davis, USA
- Head's Wild Tree Tech, Switzerland

Poster presented at [RECOMB 2017][1].

## Abstract

MinHashes can be used to estimate the similarity of two or more datasets.
Expanding on the work pioneered by mash and extended in our library Sourmash,
we calculated signatures for 412 thousand microbial reads datasets on the Sequence Read Archive.
To be able to efficiently search for matches of these signatures in the RefSeq microbial genomes database we developed a new data structure based on Sequence Bloom Trees adapted for searching MinHash signatures (named SBTMH) and made it available to whoever wants to use it.

We explore how to encode the SBTMH structure as objects in a MerkleDAG and store it in IPFS (InterPlanetary File System),
a decentralized system for data sharing, and how to load and spread the SBTMH indexes as well as the signatures calculated.
The SBTMH behaves like a persistent data structure,
where updates and new nodes can share parts of the structure of previous versions of the SBTMH.
While this property can be used to avoid duplicating data,
in this case it is important because it allows common nodes in trees to be shared,
leading to increased availability and facilitating sharing and remixing of indexes and signatures.

This design can be extended to change how databases and archives (like the SRA) are offered and implemented,
since users can collaborate by choosing to share subsets of the archive and spread the network bandwidth.
More importantly,
it avoids the central point of failure,
while still allowing for curation and quality assurance of the data.
We present a prototype showing how this can be achieved.

## Table of Contents

- [Introduction](01.intro.md)
- [Saving a SBTMH in IPFS](02.saving.md)
- [Sharing datasets in IPFS](03.sharing.md)
- [Future work](04.future.md)
- [References](#references)
- Appendices
  - [Submitted abstract](abstract.md)
  - [The final poster](poster/poster.pdf)

## References

- Benet, Juan. 2014. “IPFS - Content Addressed, Versioned, P2P File System.” arXiv:1407.3561 [Cs], July. http://arxiv.org/abs/1407.3561.
- Broder, Andrei Z. 1997. “On the Resemblance and Containment of Documents.” - In Compression and Complexity of Sequences 1997. Proceedings, 21–29. IEEE. http://ieeexplore.ieee.org/abstract/document/666900/.
- GB Editorial Team. 2011. “Closure of the NCBI SRA and Implications for the Long-Term Future of Genomics Data Storage.” Genome Biology 12: 402. doi:10.1186/gb-2011-12-3-402. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3129670/
- Driscoll, James R., Neil Sarnak, Daniel D. Sleator, and Robert E. Tarjan. 1989. “Making Data Structures Persistent.” Journal of Computer and System Sciences 38 (1): 86–124. https://dx.doi.org/10.1016/0022-0000(89)90034-2
- Ondov, Brian D., Todd J. Treangen, Páll Melsted, Adam B. Mallonee, Nicholas H. Bergman, Sergey Koren, and Adam M. Phillippy. 2016. “Mash: Fast Genome and Metagenome Distance Estimation Using MinHash.” Genome Biology 17: 132. https://dx.doi.org/10.1186/s13059-016-0997-x
- Solomon, Brad, and Carl Kingsford. 2016. “Fast Search of Thousands of Short-Read Sequencing Experiments.” Nature Biotechnology 34 (3): 300–302. https://dx.doi.org/10.1038/nbt.3442
- Titus Brown, C., and Luiz Irber. 2016. “sourmash: A Library for MinHash Sketching of DNA.” The Journal of Open Source Software 1 (5). https://dx.doi.org/10.21105/joss.00027


[1]: http://cb.csail.mit.edu/cb/recomb2017/
