# Huffman Coding Compression Algorithm

## Overview
This project implements the Huffman coding compression algorithm in Python. Huffman coding is a widely used technique for lossless data compression. It works by assigning variable-length codes to input characters, with shorter codes assigned to more frequent characters. This compression technique is particularly efficient for text files, as characters with higher frequencies are encoded with shorter codes, resulting in reduced file size.

## Features
- **Compression**: Given an input file, the program compresses it using Huffman coding and generates a binary file with the compressed data.
- **Decompression**: The program can decompress the compressed binary file back to its original form.

## How it Works
1. **Frequency Calculation**: The frequency of each character in the input text file is calculated using a Python Counter.
2. **Building Huffman Tree**: A binary tree is constructed using a priority queue (heapq) where each node represents a character along with its frequency. Huffman coding works by combining the two nodes with the lowest frequencies at each step until there is only one node left, which becomes the root of the Huffman tree.
3. **Generating Huffman Codes**: Once the Huffman tree is built, the program traverses the tree to generate Huffman codes for each character. These codes are used for encoding the original text.
4. **Encoding**: The original text is encoded using the generated Huffman codes. The encoded text is padded to ensure it is a multiple of 8 bits.
5. **Compression**: The padded encoded text is converted into bytes and written to a binary file.
6. **Decompression**: To decompress the binary file, the program reads the bytes and converts them back to bits. It removes the padding and decodes the Huffman-encoded text using the Huffman tree.
7. **Writing Decompressed Text**: The decompressed text is written to an output text file.

## Usage
1. Run the script and provide the path to the file you want to compress.
2. The compressed file will be generated in the same directory with a ".binary" extension.
3. To decompress the file, run the script again and provide the path to the compressed file. The decompressed file will be generated with "_decompressed.txt" appended to the original filename.

## Author
- **Author**: [Akshay Parihar](https://github.com/Akshayparihar07)

## Dependencies
- Python 3.x
