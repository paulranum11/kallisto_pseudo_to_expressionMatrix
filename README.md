# kallisto_pseudo_to_expressionMatrix
Use this tool to convert the output of kallisto pseudo into a equivalence class counts matrix suitable for input into Seurat.

# About
This tool was created because I was unable to extract a Seurat compatable expression matrix from the output of kallisto "pseudo". It relies on modified version of the "prep_TCC_matrix.py" script written by the pachterlab https://github.com/pachterlab/scRNA-Seq-TCC-prep

# Usage
Example usage is as follows:

python3 prep_TCC_matrix.py -T matrix.tsv -E matrix.ec -O outputDir -I Mus_musculus.GRCm38.cdna.all.fa

# Options
-E | --inputMatrixec # Provide the "matrix.ec" file output by kallisto "pseudo" 

-T | --inputMatrixtsv # Provide the "matrix.tsv" file output by kallisto "pseudo"

-O | --outputDir # Provide the path to your desired output directory

-I | --indexFasta # Provide the path to the index .fasta file that was used to generate your kallisto .idx file.  This file must be unzipped


