# Grep Tutorial for Linux Terminal

This tutorial introduces the `grep` command, a powerful tool for searching text in files. We'll focus on examples using FASTA files, common in bioinformatics for storing DNA sequences. FASTA files contain sequences prefixed with a header line starting with `>`.

Assume we have a sample FASTA file named `sequences.fasta` with content like:

```
>sequence1
ATCGATCGATCG
>sequence2
GCTAGCTAGCTA
>sequence3
TTTTAAAA
```

## Basic Search

### Search for a string in a file
```bash
grep "search_string" filename
```
**Explanation:** Searches for exact matches of "search_string" in the file.  
**Example:** Search for "ATCG" in `sequences.fasta`:  
```bash
grep "ATCG" sequences.fasta
```
**Output:**  
```
ATCGATCGATCG
```

### Case-insensitive search
```bash
grep -i "search_string" filename
```
**Explanation:** Ignores case differences.  
**Example:** Search for "atcg" (case-insensitive) in `sequences.fasta`:  
```bash
grep -i "atcg" sequences.fasta
```
**Output:**  
```
ATCGATCGATCG
```

## Recursive and Inverse Searches

### Search recursively in a directory
```bash
grep -r "search_string" directory
```
**Explanation:** Searches in all files within the directory and subdirectories.  
**Example:** Search for "ATCG" in the current directory (assuming `sequences.fasta` is there):  
```bash
grep -r "ATCG" .
```
**Output:**  
```
sequences.fasta:ATCGATCGATCG
```

### Invert match (show lines without the string)
```bash
grep -v "search_string" filename
```
**Explanation:** Displays lines that do not contain the string.  
**Example:** Show lines in `sequences.fasta` without "ATCG":  
```bash
grep -v "ATCG" sequences.fasta
```
**Output:**  
```
>sequence1
>sequence2
GCTAGCTAGCTA
>sequence3
TTTTAAAA
```

## Counting and Line Numbers

### Count matching lines
```bash
grep -c "search_string" filename
```
**Explanation:** Counts the number of lines containing the string.  
**Example:** Count lines with "ATCG" in `sequences.fasta`:  
```bash
grep -c "ATCG" sequences.fasta
```
**Output:**  
```
1
```

### Show line numbers
```bash
grep -n "search_string" filename
```
**Explanation:** Displays matching lines with their line numbers.  
**Example:** Find line numbers for "ATCG" in `sequences.fasta`:  
```bash
grep -n "ATCG" sequences.fasta
```
**Output:**  
```
2:ATCGATCGATCG
```

### List files containing the string
```bash
grep -l "search_string" filename
```
**Explanation:** Lists filenames that contain the string (useful for multiple files).  
**Example:** List files containing "ATCG" (run on `sequences.fasta`):  
```bash
grep -l "ATCG" sequences.fasta
```
**Output:**  
```
sequences.fasta
```

## Extended Regular Expressions (for DNA Sequences)

### Search for any nucleotide (A, T, C, G)
```bash
grep -E "A|T|C|G" filename
```
**Explanation:** Uses extended regex to match any single nucleotide.  
**Example:** Find any nucleotide in `sequences.fasta` (matches all sequence lines):  
```bash
grep -E "A|T|C|G" sequences.fasta
```
**Output:**  
```
ATCGATCGATCG
GCTAGCTAGCTA
TTTTAAAA
```

### Search for exact sequence
```bash
grep -E "ATCG" filename
```
**Explanation:** Matches the exact string "ATCG".  
**Example:** Same as basic search for "ATCG" in `sequences.fasta`:  
```bash
grep -E "ATCG" sequences.fasta
```
**Output:**  
```
ATCGATCGATCG
```

### Search for dinucleotide repeats (AA, TT, CC, GG)
```bash
grep -E "A{2,}|T{2,}|C{2,}|G{2,}" filename
```
**Explanation:** Matches two or more consecutive identical nucleotides.  
**Example:** Find repeats in `sequences.fasta`:  
```bash
grep -E "A{2,}|T{2,}|C{2,}|G{2,}" sequences.fasta
```
**Output:**  
```
TTTTAAAA
```

### Search for trinucleotide repeats (AAA, TTT, CCC, GGG)
```bash
grep -E "A{3,}|T{3,}|C{3,}|G{3,}" filename
```
**Explanation:** Matches three or more consecutive identical nucleotides.  
**Example:** Find longer repeats in `sequences.fasta`:  
```bash
grep -E "A{3,}|T{3,}|C{3,}|G{3,}" sequences.fasta
```
**Output:**  
```
TTTTAAAA
```

These examples demonstrate `grep` for analyzing FASTA files in bioinformatics. Practice with your own files to explore patterns in DNA sequences.