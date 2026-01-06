# Prompt

Act as a bioinformatician: please provide a script that performs the following tasks.

1. Copy the short reads (.fastq.gz) from this path:

   `/home/jamal/03_wgs_assembly/hybrid_genome_assembly_guide/01_raw_reads/short_reads`

   into a new directory here called `00_raw_reads`.

2. Create the following directories in the current project directory:

   - `01_qc_before_processing`
   - `02_process_reads`
   - `03_qc_after_processing`

See `analysis.sh` for an idempotent Bash script that implements these steps and usage instructions.
