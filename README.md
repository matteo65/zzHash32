#zzHash32 – A High-Performance Non-Cryptographic Hash Function  

This project represents the culmination of over five years of dedicated research focused on the design and development of new non-cryptographic hash functions.

During this period, I developed a large suite of statistical data analysis tools, designed and tested dozens of original hash functions, wrote thousands of lines of experimental and production-grade code, and conducted extensive validation against theoretical and empirical benchmarks. The goal throughout this research was clear: to approach the statistical behavior of an Ideal Hash Function while maintaining practical efficiency.

Two complete families of hash functions were previously released:

ZeeMeeHash (32-bit and 64-bit)  
MzHash (32-, 64-, 128-, and 192-bit)

Both families are available in their respective GitHub repositories. These functions achieve an output distribution extremely close to the theoretical ideal, demonstrating excellent avalanche behavior, uniformity, and resistance to statistical bias.

However, the MzHash family processes input byte-by-byte. While still very fast, this design choice makes direct performance comparisons difficult against block-based hash functions such as XXHash or MurmurHash, which process input in grouped byte blocks.

Introducing zzHash32

zzHash32 is the natural evolution of this research.

The objective behind zzHash32 was to preserve the conceptual simplicity and structural elegance of mzHash32 while introducing block-based processing to significantly improve throughput.

Unlike its predecessor, zzHash32 processes input data in 4-byte blocks. This architectural shift allows it to compete directly with modern high-performance non-cryptographic hash functions while maintaining the statistical strengths developed through years of research.

Key Characteristics

32-bit non-cryptographic hash function

Processes input in 4-byte blocks

Extremely high execution speed

Excellent statistical distribution

Output quality very close to the Ideal Hash Function model

Clean and simple internal structure

The result is a hash function that combines:

The statistical rigor of the MzHash design philosophy

The performance advantages of block-based hashing

A minimalist and efficient implementation

zzHash32 delivers both speed and quality, making it suitable for hash tables, indexing systems, data structures, checksums, and other high-performance non-cryptographic use cases.

This function represents not just a new implementation, but the synthesis of years of experimentation, statistical validation, and iterative refinement in the field of non-cryptographic hashing.
