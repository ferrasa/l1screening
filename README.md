# L1Screening

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![DOI](https://img.shields.io/badge/DOI-L1Farm--Paper--DOI-blue)](https://doi.org/your-l1farm-paper-doi)

A bioinformatics pipeline for the comprehensive identification, annotation, and assembly of LINE-1 (L1) retrotransposons in reference and personal genomes.

## About The Project

`L1Screening` was designed to overcome the limitations of standard repeat annotation software by providing a detailed, multi-layered analysis of L1 elements.

It systematically processes genomic data to:
*   Identify L1 elements belonging to multiple subfamilies.
*   Annotate specific L1 regions (5'UTR, ORF1, intron, ORF2, 3'UTR).
*   Filter results based on sequence identity and similarity.
*   Resolve redundant annotations for overlapping loci.
*   Assemble full-length L1 elements from their constituent fragments.

The pipeline is versatile and can be applied to any FASTA-formatted genome, making it a valuable resource for studying the impact of transposable elements on genome structure and evolution.

### Key Features

*   **Comprehensive Identification:** Detects elements from 18 different L1 subfamilies.
*   **Detailed Annotation:** Provides segment-level information for both full-length and partial L1 insertions.
*   **High Accuracy:** Uses a consensus-based approach to resolve conflicting annotations.
*   **Full-Length Assembly:** Includes a custom module (`FL-Assemble` logic) to identify intact L1 elements.
*   **Flexible:** Can be adapted for both reference genomes (e.g., Hg38) and individual, diploid genomes.

## Getting Started

### Prerequisites

This pipeline requires the following software to be installed and available in your system's PATH:
*   [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)
*   Python 3.7+
*   Conda (recommended for managing environments)

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/ferrasa/l1screening.git
    cd l1screening
    ```

2.  **Create and activate a Conda environment (recommended):**
    ```sh
    conda env create -f environment.yml
    conda activate l1screening
    ```
    *(You will need to create an `environment.yml` file with the dependencies: `python`, `pandas`, `pysam`, `biopython`, etc.)*

## Usage

The pipeline follows a multi-step process. Please refer to the manuscript for detailed methodology.

1.  **Prepare your directories** and input files as described in the documentation.
2.  **Generate L1 fragments** from your consensus sequences.
3.  **Run the Bowtie2 alignment** against your target genome.
4.  **Process the alignments** and generate the final L1Farm databases using the main Python script.

*Detailed execution commands and examples will be provided upon the official release of the software.*

## Citation

If you use `L1Screening` or the L1Farm database in your research, please cite our paper:

> Unpublished

A manuscript detailing the `L1Screening` software is currently in preparation. Please check back for updates on its citation.

## License

Distributed under the MIT License. See `LICENSE.md` for more information.
