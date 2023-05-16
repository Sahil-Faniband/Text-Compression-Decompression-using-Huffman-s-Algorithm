# Text-Compression-Decompression-using-Huffman-s-Algorithm
 This is a C++ program that implements Huffman coding for text compression and decompression. The input string that needs to be compressed and decompressed using Huffman coding. 
 
 
 
Huffman’s algorithm:-
The Huffman algorithm is a popular method for lossless data compression. It assigns variable-length binary codes to different characters or symbols based on their frequency of occurrence in the input data. Here's an explanation of the Huffman algorithm:

1)Character Frequency Calculation: The algorithm starts by analyzing the input data and counting the frequency of each character or symbol. This step builds a frequency table that records how often each character appears in the input.

2)Creating Huffman Trees: Based on the frequency table, the Huffman algorithm constructs a series of binary trees. Initially, each character is treated as a single-node tree. Then, the two trees with the lowest frequencies are combined into a new tree with a shared parent node. This process is repeated until all the individual trees are merged into a single tree called the Huffman tree.

3)Assigning Codes: In the Huffman tree, each character or symbol is associated with a unique binary code. The codes are assigned by traversing the tree from the root to each leaf node. When moving to the left child, a '0' is appended to the code, and when moving to the right child, a '1' is appended. The codes assigned to the characters are constructed in such a way that no code is a prefix of another code, ensuring unambiguous decoding.

4)Encoding: With the assigned binary codes, the input data is encoded by replacing each character with its corresponding code. This results in a compressed representation of the original data, where frequently occurring characters are represented by shorter codes.

To illustrate the encoding process, consider an example where the characters 'A', 'B', 'C', and 'D' have the following frequencies: 'A' (4 times), 'B' (2 times), 'C' (1 time), and 'D' (1 time). The Huffman algorithm would construct a tree like this:

    * (root)
   / \
  A   *
     / \
    B   *
       / \
      C   D
Based on this tree, the following codes would be assigned:

A: 0
B: 10
C: 110
D: 111

So, if the original input was "AABCD", the compressed representation using Huffman encoding would be "010110111".

Decompression involves using the same Huffman tree and codes to reverse the process. The compressed data is read bit by bit, starting from the root of the Huffman tree. When a '0' is encountered, the left child is followed, and when a '1' is encountered, the right child is followed. When a leaf node is reached, the corresponding character is output, and the process continues until all the compressed data is processed, reconstructing the original data.

In summary, the Huffman algorithm uses frequency-based encoding to compress data efficiently, assigning shorter codes to more frequent characters and longer codes to less frequent characters. This enables effective storage and transmission of data while preserving its content.
