This repository contains a phylogenetic tree of LAR and other PIP family enzymes as shown in Güngör et al. 2020: Azolla ferns testify: seed plants and ferns share a common ancestor for leucoanthocyanidin reductase enzymes (link will follow upon publication). 
Additionally, this repository details all code and intermediate files used in the process towards that tree.

### Quick links:
Phylogeny of LAR and LAR likes in plants:
 *  [treefile](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/analyses/1kP_LAR_selectionv1_guide_v5_trees/aligned-mafft-linsi_trim-gt4-seq95-res7/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi_trim-gt4-seq95-res7_iqtree-bb2000-alrt2000.treefile) 
 * main text figure 
 [png](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets_600.svg.png), 
 [pdf](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets.pdf) & 
 [Inkscape_svg](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4_brackets.svg)  
 * supplemental figure 
  [pdf](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/supporting_information/LAR_orthogroup_selectionv1_guide_v5_SHaLRT_long_inpage_v3.pdf) & 
  [Inkscape_svg](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/supporting_information/LAR_orthogroup_selectionv1_guide_v5_SHaLRT_long_inpage_v3.svg) 

Final alignment: [raw](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/alignments_raw/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi.fasta) 
& [trimmed](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/alignments_trimmed/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi_trim-gt4-seq95-res7.fasta)

Final fasta used for alignment:
 * the [complete fasta](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/1kP_LAR_selectionv1_guide_v5.fasta) file
 * a [selection from the 1kP orthogroup](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/1kP_LAR_orthogroup_manual-selection-1.fasta) 
 * a manually composed set of [guide sequences](https://github.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/blob/main/data/Erbils_guide_v3.fasta) to annotate and interpret the tree.
 
### Final figure as shown in Güngör et al. 2020
![PIP enzymes and LAR phylogenetic tree](https://media.githubusercontent.com/media/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets_600.svg.png)  

### Guide through folders and files
The `data` folder contains (unaligned) fasta files, lists of sequence names, and aligned sequences in both trimmed and untrimmed versions. 
File names tend to be long, but are meant to reflect the history of that specific file. 
For example: `1kP_LAR_orthogroup_manual-selection-1_guidev4_aligned-mafft-linsi_trim-gt6-seq80.fasta` contains sequences from the 1kP LAR orthogroup from which a manual selection was taken. 
Second, a set of guide sequences (sequences whose function has been verified) was added.
These sequences were then aligned with mafft-linsi and trimmed with trimAL settings `-gt .6 and -seq 80.`

The `analyses` folder contains tree inferences. 
These are organised in folders of starting dataset, and then in folders of alignment and trimming strategy.
Still, a folder may contain several tree inferences made with IQTree. 
The final part of the filename summarises the settings used to create a particular tree file. 
Note that intermediate trees are just that, intermediate results. 
The `fernLARclades_analyses` directory contains tree inferences on specifically the fern LAR, WLAR1 and WLAR2 clades as shown in figure 8 of Güngör _et al_. 2020.

The `figures` folder contains the final versions of the figures shown in Güngör _et al_. in several formats. 
These were made by importing a `.treefile` in [iToL](https://itol.embl.de/), then adding annotation manually, and downloading these as `.svg` file.
These `.svg` files were then finalised in Inkscape to their published form and exported as pdf or png. 

The workflows for which data is shared here, are documented in JuPyter notebooks (`*.ipynb`).
The workflow describing the final version of the tree is [tree_building_workflow_v5](https://github.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/blob/main/tree_building_workflow_v5.ipynb). 
The other two workflows are explorative and should be interpreted as such. Note that figures which are embedded in the JuPyter notebooks are not properly displayed online on Github. You may download the `.ipynb` files to display them locally, including images.

### Data sources used in this project
In building these trees, we have made use of publicly available data exclusively. 
Except perhaps, for two _Azolla filiculoides_ sequences for which we have manually corrected the automated annotation.
_Azolla_ automated annotations are available on [fernbase](ftp://ftp.fernbase.org/Azolla_filiculoides/Azolla_asm_v1.1/)
The manually annotated sequences used here were submitted to EBI's [ENA](https://www.ebi.ac.uk/ena/browser/home) under study accession number [PRJEB39515](https://www.ebi.ac.uk/ena/browser/view/PRJEB39515).
These sequences are also hosted in this github repository as 
[nucleotide](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/AzfiLAR_ENA-submission.fna) 
and 
[protein](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/AzfiLAR_ENA-submission.faa) 
fasta files. 

Notably, we have made use of data made available by the [1000 plant transcriptomes project](https://sites.google.com/a/ualberta.ca/onekp/) (1kP).
First, we made use of the [1kP orthogroup extractor](http://jlmwiki.plantbio.uga.edu/onekp/v2/) to extract a LAR orthogroup by providing it with the _Vitis vinifera_ LAR sequence. 
Second, we made use of the online [sample list viewer](http://www.onekp.com/samples/list.php) to create a subset of the 1kP PIP enzyme orthogroup; taking care to sample across the tree of all plants with extra attention to seed-free plants. 
The subset used here is online in [google sheets](https://docs.google.com/spreadsheets/d/1v2igxY_nr7ETMoUdbqpY0QKVxJ-KYiRiO2lLoyOABsw/edit?usp=sharing), and the resulting lists are stored here in the `data` directory.

The 1kP project provides a wealth of sequencing information on taxa of plants for which few sequences are available from genome sequences, let alone sequences of which their function is verified. 
Therefore, we thankfully made use of the sequences collected in literature and online databases; 
most notably so in Koeduka's paper 'Functional evolution of biosynthetic enzymes that produce plant volatiles' published in 'Bioscience, Biotechnology, and Biochemistry' in 2018.
Each of these sequences and their original accession number are listed in [this fasta file](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/Erbils_guide_v3.fasta).
 
