# RNA-seq Nextflow Pipeline  
The script owner's @shaimaa672
## 📌 Overview  
A reproducible and scalable **RNA-seq preprocessing pipeline** implemented in **Nextflow**, automating trimming, quality control, alignment, and quantification. The pipeline ensures reproducibility and efficiency for bioinformatics research, supporting both local and cloud/HPC execution.  

---

## 🧠 Objectives  
- Automate RNA-seq preprocessing from raw FASTQ to count matrix.  
- Support multiple aligners (HISAT2, Bowtie2).  
- Ensure reproducibility across different environments.  
- Produce clean, analysis-ready data for downstream tools like DESeq2 or edgeR.  

---

## ⚙️ Tech Stack  
- **Languages:** Nextflow DSL2, Bash  
- **Tools:** Cutadapt, FastQC, HISAT2, Bowtie2, featureCounts  
- **Deployment:** Local machine, HPC (SLURM), AWS Batch  

---

## 📂 Workflow  
1. **Trimming** – Remove adapter sequences with **Cutadapt**.  
2. **Quality Control** – Assess read quality with **FastQC**.  
3. **Alignment** – Map reads to reference genome using **HISAT2** or **Bowtie2**.  
4. **Quantification** – Generate read count matrix using **featureCounts**.  

---

## 🚀 Results  
- Fully automated from raw FASTQ files to count matrix.  
- Parallelized execution reduces runtime by up to **60%** on HPC clusters.  
- Modular configuration for easy parameter adjustments.  

---

## 📦 Installation & Usage  

```bash
# Clone the repository
git clone https://github.com/yusufharb/rnaseq-nextflow-pipeline.git
cd rnaseq-nextflow-pipeline

# Run pipeline
nextflow run main.nf \
  --reads 'data/*.fastq.gz' \
  --genome 'reference/genome.fa'
