#### Short-Read Genome Assembly Pipeline
A production-ready workflow for Illumina paired-end data

## Overview
This repository provides an end-to-end, reproducible pipeline that converts raw Illumina reads into a high-quality, annotated bacterial genome.
- Illumina paired-end reads → quality trim → SPAdes assembly → CheckM2/QUAST/BUSCO QC → Prokka/Bakta annotation.

<img width="1547" height="466" alt="short_read_assembly_map" src="https://github.com/user-attachments/assets/d2b6b55e-a6a3-4a57-a196-59111ca0d6fa" />

## Pipeline Steps & Quick Start
git clone https://github.com/jamal-20/short_reads_only_assembly.git
cd short-read-assembly
See `installation.sh` for an idempotent Bash script that implements these steps and usage instructions.
See `analysis.sh` for an idempotent Bash script that implements these steps and usage instructions.

## Repository Structure & Output

| Directory                       | Key Files                                                                                 | Purpose                                     |
| ------------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------- |
| `01_qc_before_processing/`      | `multiqc/`                                                                                | Pre-trimming quality                        |
| `02_process_reads/`             | `*processed.fastq.gz`                                                                     | Cleaned reads                               |
| `03_qc_after_processing/`       | `multiqc/`                                                                                | Post-trimming quality                       |
| `04_short_reads_only_assembly/` | `spades_output/scaffolds.fasta`                                                           | Final assembly                              |
| `05_genome_quality_assessment/` | `01_checkm2/quality_report.tsv`<br>`02_quast/report.html`<br>`04_busco/short_summary.txt` | Completeness, contiguity, lineage integrity |
| `06_genome_annotation/`         | `01_prokka_annotation/` (GBK, FAA)<br>`02_bakta_annotation/` (GBF, TSV)                   | Functional & structural annotation          |

## Citation
FastQC, FastP, SPAdes, CheckM2, QUAST, BUSCO, Prokka, Bakta.
