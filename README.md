# CQ-Exam

### Agnes Oetting
### 10.05.2023
### NGS-Scripting; First Steps

## Description:
### Before you start: 
- Create the folder: "singularity-container" in your working directory
- Create the folder "SRA_data"
- You need to have the sra-toolkit installed (https://github.com/ncbi/sra-tools)
- Configure sra-toolkit (user repository: home/cq/NGS/cq-examples/exam/SRA_data)

### To run the script
The user can change accession number and output directory (default: "SRA_data").

You run the script via (example):
nextflow run ....nf --accession SRR11192680 -profile singularity
### What does the script do:
It uses 4 predefinded processes which are imported by include { xxx } from "yyy":

prefetch: downloads all necessary sra files (depending on accession number) in ".../SRA_data/sra/accession.sra"

fastq-dump: Extracts fastq-file(s) from SRA-accessions

fastqc: check the quality of our sequence reads, creates ".*html" and "*.zip" file

fastp: Fastp provides fast all-in-one preprocessing for FastQ files (trimming, creates report)
