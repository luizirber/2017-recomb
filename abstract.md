<!-- https://easychair.org/conferences/?conf=recomb2017 -->

# Title

Decentralized indexes for public genomic data

# Abstract

MinHashes can be used to estimate the similarity of two or more datasets.
Expanding on the work pioneered by mash and extended in our library Sourmash,
this poster presents a new data structure based on Sequence Bloom Trees adapted for searching MinHash signatures.

It also explores how to encode SBTs as objects in a MerkleDAG in IPFS and store it in IPFS,
a decentralized system for data sharing.
This allows easy sharing and remixing of indexes,
including versioning and persistence of data even if the original seeder is gone.

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


