# RNA-Seq-pipeline
A Python-native RNA-seq analysis pipeline for quality control, read trimming, normalization, and differential expression. Built with pandas, NumPy, Biopython, and pysam, with optional STAR/Salmon integration. Lightweight, modular, and educational for RNA-seq workflows.


## Features
- FASTQ quality control (Python-based FastQC-like analyzer)
- Read trimming by quality and length
- Normalization: RLE, TPM, CPM
- Simple differential expression analysis (fold change + t-test with FDR correction)
- Automatic QC plots and HTML summary report
- Optional integration with STAR/Salmon/featureCounts

---

## Requirements
Install dependencies:
```bash
pip install -r requirements.txt
pandas
numpy
matplotlib
seaborn
biopython
pysam
pyfaidx
scipy
statsmodels
```

## Usage

Run the pipeline with:

python pipeline.py --input-dir raw_data/ --output-dir results/ --mode python


Arguments:

- config : JSON config file (optional)

- input-dir : directory containing FASTQ files

- output-dir : directory for results

- mode : python (pure Python) or hybrid (Python + external tools)

- create-config : generate a config template

- sample-info : CSV file with sample/condition info

## Outputs

- qc_raw/ and qc_trimmed/ → QC plots & summaries

- trimmed/ → trimmed FASTQ files

- reports/ → differential expression results & plots

- pipeline_report.html → summary report

## Example
- python pipeline.py --input-dir ./fastq --output-dir ./results --mode python
