<!-- https://easychair.org/conferences/?conf=recomb2017 -->

# Title

Decentralized indexes for public genomic data

# Abstract

MinHashes can be used to estimate the similarity of two or more datasets. Expanding on the work pioneered by mash and extended in our library Sourmash, we calculated signatures for 412 thousand microbial reads datasets on the Sequence Read Archive. To be able to efficiently search for matches in the RefSeq microbial genomes database we developed a new data structure based on Sequence Bloom Trees adapted for searching MinHash signatures (named SBTMH).

We also explore how to encode the SBTMH structure as objects in a MerkleDAG and store it in IPFS (InterPlanetary File System), a decentralized system for data sharing, and how to load and spread the SBTMH indexes as well as the signatures calculated. The design allows easy sharing and remixing of indexes and signatures, including versioning, persistence of data and the performance benefits of having many peers sharing data instead of a centralized infrastructure.

This design can also be extended to change how databases and archives (like the SRA) are offered for use,
...

<!--
 - Calculate minhashes signatures
 - How do distribute them?
  * IPFS and data sharing
 - Efficient search of large collections of datasets: SBTMH
  * SBT where leaves are MinHashes
 - Encoding Sequence Bloom Trees in the MerkleDAG
  * Persistent data structures: https://en.wikipedia.org/wiki/Persistent_data_structure
  * Adding new versions
 - 


-->


# Keywords


