My-Projects
DNA Sequence Analyzer

A Python-based computational tool that uses the Pandas library to read, process, and analyze genomic data from CSV files. This script automates the extraction of key sequence metrics and provides a comprehensive summary report, making it highly useful for downstream bioinformatics workflows.

Features

Data Parsing: Reads DNA sequence datasets directly from CSV formats.

Basic Metrics: Calculates sequence length and individual nucleotide counts (A, T, G, C) along with their relative frequencies.

Composition Analysis: Computes GC and AT percentages for each sequence.

Quality Control: Scans for and flags invalid characters (any character other than A, G, T, C) within the sequences.

Codon Detection: Identifies and counts occurrences of Start (ATG) and Stop (TAA, TAG, TGA) codons.

Custom Pattern Search: Prompts the user to input a specific DNA sequence pattern and counts its occurrences across the dataset.

Species-Level Aggregation: Groups data by species to provide average metrics (sequence length, GC%, AT%).

Extremes Identification: Automatically extracts the samples with the highest and lowest GC percentages.

Prerequisites

To run this script, you will need Python 3.x and the Pandas library installed on your system.

You can install Pandas using pip:

pip install pandas


Dataset Requirements

The script expects a CSV file named dna_sequence_dataset.csv in the same directory. The dataset should contain at least the following columns:

Sample_ID: A unique identifier for each sample.

Species: The species from which the DNA was sampled.

DNA_Sequence: The raw string of nucleotides.

Usage

Clone this repository or download the script.

Ensure your dataset is named dna_sequence_dataset.csv and is located in the same directory as the script.

Run the script from your terminal:

python analyzer.py


Note: The script is interactive and will prompt you in the terminal to enter a specific DNA sequence pattern you wish to search for.

Example Output

When you run the script, it generates a summary report in the terminal:

-- DNA Analysis Report --
Total Samples Analysed: 50

--- Invalid Samples Flagged ---
Sample_ID Species           DNA_Sequence Invalid_Chars
     S050 Unknown ATGCGTXACGATCGATGCTAGC             X

Samples containing invalid nucleotides: : 1

Species Comparison
           Sample_Count  Avg_Length  Avg_GC_Percent  Avg_AT_Percent
Species                                                            
Chicken               7       30.43           45.53           54.47
Frog                  7       30.57           46.73           53.27
...

Highest GC%: 53.33%
Sample_ID   Species  Length   GC%
     S003     Human      30 53.33

Lowest GC%: 41.94%
Sample_ID  Species  Length   GC%
     S037    Mouse      31 41.94


About the Author

Developed by Anvika, an undergraduate studying Biotechnology and Zoology with a focus on Computational Genomics. Actively seeking research internships and collaborations in bioinformatics and clinical genomics.
