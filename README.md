# File Compression Tool (Rust)

A simple command-line file compression tool written in **Rust**, using the `flate2` crate to compress files with the **gzip (DEFLATE)** algorithm.

The program reads a source file, compresses it using a streaming approach, and writes the compressed output to a target file. It also reports the original file size, the compressed file size, and the total time taken for the compression process.

## Features
- Command-line interface (`<source> <target>`)
- Gzip compression using `flate2`
- Buffered file reading for better performance
- Streaming compression with low memory usage
- File size comparison before and after compression
- Execution time measurement

## Usage
```bash
cargo run -- <source> <target>

Example:
cargo run -- input.txt output.gz

## Implementation Details

Uses BufReader for efficient input handling

Uses GzEncoder with default compression settings

Performs compression via std::io::copy

Measures execution time with std::time::Instant

## Purpose

This project was created as a learning exercise to practice Rust fundamentals, including file I/O, ownership and borrowing, iterators, and integrating external crates with Cargo.
