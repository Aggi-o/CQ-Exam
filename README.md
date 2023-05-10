# CQ-Exam

## Agnes Oetting
## 10.05.2023
## NGS-Scripting; First Steps

## What does the script do:
The user can change accession number and output directory (default: "SRA_data").

You run the script via (example):
nextflow run ....nf --accession SRR11192680 -profile singularity

It uses 4 predefinded processes which are imported by include { xxx } from "yyy":

prefetch: downloads all necessary sra files (depending on accession number) in ".../SRA_data/sra/accession.sra"

fastq-dump: Extracts fastq-file(s) from SRA-accessions

fastqc: check the quality of our sequence reads, creates ".*html" and "*.zip" file

fastp: Fastp provides fast all-in-one preprocessing for FastQ files (trimming, creates report)
