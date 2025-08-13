# Protein-Protein Interaction Prediction Project

## Overview
This project focuses on predicting protein-protein interactions (PPIs) using machine learning techniques and bioinformatics analysis. The goal is to classify protein sequence pairs as either interacting (positive) or non-interacting (negative) based on various protein sequence features.

## Project Structure
```
Project/
├── README.md                           # This file
├── Project.ipynb                       # Main Jupyter notebook with analysis
├── positive_protein_sequences.csv      # Dataset of positive (interacting) protein pairs
└── negative_protein_sequences.csv      # Dataset of negative (non-interacting) protein pairs
```

## Dataset Description
The project uses two main datasets:
- **Positive Protein Sequences**: Contains protein sequence pairs that are known to interact
- **Negative Protein Sequences**: Contains protein sequence pairs that are known not to interact

Each dataset contains two columns:
- `protein_sequences_1`: First protein sequence in the pair
- `protein_sequences_2`: Second protein sequence in the pair

## Features Extracted
The analysis extracts several important features from protein sequences:

### 1. Basic Sequence Features
- **Sequence Length**: Length of each protein sequence
- **Molecular Weight**: Calculated molecular weight using BioPython

### 2. Amino Acid Composition Features
- **Amino Acid Percentages**: Percentage composition of all 20 standard amino acids for each sequence
- Features are prefixed with `aac1_` for the first sequence and `aac2_` for the second sequence

### 3. Protein Properties
- **Aromaticity**: Aromatic amino acid content in the sequences
- Additional physicochemical properties can be calculated using BioPython's ProteinAnalysis

## Dependencies
The project requires the following Python packages:
- `pandas` - For data manipulation and analysis
- `biopython` - For protein sequence analysis and feature extraction
- `numpy` - For numerical computations

## Installation
```bash
pip install pandas biopython numpy
```

## Usage
1. Open `Project.ipynb` in Jupyter Notebook or JupyterLab
2. Run the cells sequentially to:
   - Load the protein sequence datasets
   - Extract features from protein sequences
   - Prepare the data for machine learning
   - Perform analysis and predictions


## Data Preprocessing
The project includes several preprocessing steps:
1. **Label Assignment**: Positive sequences labeled as 1, negative as 0
2. **Data Concatenation**: Combining positive and negative datasets
3. **Random Shuffling**: Randomizing the order of samples
4. **Feature Engineering**: Creating new features from protein sequences

