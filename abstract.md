<!-- https://easychair.org/conferences/?conf=recomb2017 -->

# Title

Decentralized indexes for public genomic data

# Abstract

MinHashes can be used to estimate the similarity of two or more datasets. Expanding on the work pioneered by mash and extended in our library Sourmash, we calculated signatures for 412 thousand microbial reads datasets on the Sequence Read Archive. To be able to efficiently search for matches of these signatures in the RefSeq microbial genomes database we developed a new data structure based on Sequence Bloom Trees adapted for searching MinHash signatures (named SBTMH) and made it available to whoever wants to use it.

We explore how to encode the SBTMH structure as objects in a MerkleDAG and store it in IPFS (InterPlanetary File System), a decentralized system for data sharing, and how to load and spread the SBTMH indexes as well as the signatures calculated. The SBTMH behaves like a persistent data structure, where updates and new nodes can share parts of the structure of previous versions of the SBTMH. While this property can be used to avoid duplicating data, in this case it is important because it allows common nodes in trees to be shared, leading to increased availability and facilitating sharing and remixing of indexes and signatures.

This design can be extended to change how databases and archives (like the SRA) are offered and implemented, since users can collaborate by choosing to share subsets of the archive and spread the network bandwidth. More important, it avoids the central point of failure, while still allowing for curation and quality assurance of the data. We present a prototype showing how this can be achieved.

# Keywords

similarity
minhash
decentralized
persistent data structures
sequence bloom trees
data sharing
databases
