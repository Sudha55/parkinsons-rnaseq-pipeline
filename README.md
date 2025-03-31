Parkinson's Disease RNA-Seq Analysis Pipeline
A reproducible pipeline for identifying differentially expressed genes (DEGs) in Parkinson’s disease using RNA-Seq data.

### Overview

This project automates RNA-Seq data processing, differential expression analysis, and visualization for Parkinson’s disease research. It includes:

Bash pipeline for QC, alignment, and quantification.
SQLite database to store sample metadata and DEG results.
Python/Jupyter scripts for statistical analysis and visualization.
Key Features:
1. Reproducible: Version-controlled with explicit dependencies.
2. Scalable: Designed for small datasets but extensible.
3. Documented: Step-by-step instructions for beginners.

### Setup

Prerequisites

Linux/macOS (Tested on Odin/Ubuntu 20.04).
Conda (for dependency management).
Installation

Clone this repository:
bash
Copy
git clone https://github.com/yourusername/parkinsons-rnaseq-pipeline.git
cd parkinsons-rnaseq-pipeline
Create and activate the Conda environment:
bash
Copy
conda env create -f docs/requirements.txt
conda activate rnaseq-pd
Download reference genomes (e.g., HISAT2 index for hg38):
bash
Copy
mkdir -p references/
wget -P references/ ftp://ftp.ccb.jhu.edu/pub/infphilo/hisat2/data/hg38.tar.gz
tar -xzvf references/hg38.tar.gz -C references/

### Usage

1. Run the Pipeline

Execute the Bash script to process raw FASTQ files:

bash
Copy
bash scripts/pipeline.sh
Input: FASTQ files in data/raw/.
Output: Aligned counts in data/processed/counts.txt.

2. Perform DEG Analysis

📜 License

This project is licensed under the MIT License. See LICENSE for details.

📬 Contact

Your Name: sudhapandey@unomaha.edu
GitHub Issues: Report bugs/requests here.
