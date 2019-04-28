# ngs2-assignment
 source activate  ngs1
 mkdir ~/workdir/assignment2
 cd ~/workdir/assignment2
wget http://genomedata.org/rnaseq-tutorial/fasta/GRCh38/chr22_with_ERCC92.fa
#1. Mapping to the reference
conda install star
genomeDir=~/workdir/assignment2/chr22
mkdir $genomeDir
STAR --runMode genomeGenerate --genomeDir $genomeDir --genomeFastaFiles ~/workdir/assignment2/chr22/chr22_with_ERCC92.fa --runThreadN 1
