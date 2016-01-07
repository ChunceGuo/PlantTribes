# PlantTribes Tutorial
This tutorial uses the test data `assembly.fasta`, a small set of *de novo* transcriptome contigs, in the [test](../test) subdirectory of PlantTribes installation to show how to perform an analysis using the various pipelines of PlantTribes.

### AssemblyPostProcesser Pipeline
1). The following command will post processes `assembly.fasta` using ESTScan coding regions prediction method with aid of Arabidopsis thaliana  references matrices in strand specific mode, and removes similar (sub)sequences and sequences shorter than 200 bp.

`PlantTribes/pipelines/AssemblyPostProcesser  --transcripts assembly.fasta --prediction_method estscan --score_matrices /path/to/score/matrices//Arabidopsis_thaliana.smat --strand_specific --dereplicate --min_length 200`

2). The following command as in 1) above will post processes `assembly.fasta` using TransDecoder coding regions prediction method in strand specific mode, and remove similar (sub)sequences and sequences shorter than 200 bp.

`PlantTribes/pipelines/AssemblyPostProcesser  --transcripts assembly.fasta --prediction_method transdecoder --dereplicate --min_length 200`
