This repository contains phylogenetic trees of LAR and LAR like proteins as described in Güngör et al. 2020 (link will follow upon publication). 
Additionally, this repository lists all code and intermedidate files made in the process towards that tree.

### Quick links:
Phylogeny of LAR and LAR likes in plants:
 *  [treefile](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/analyses/1kP_LAR_selectionv1_guide_v5_trees/aligned-mafft-linsi_trim-gt4-seq95-res7/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi_trim-gt4-seq95-res7_iqtree-bb2000-alrt2000.treefile) 
 * main text figure 
 [png](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets_600.svg.png), 
 [pdf](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets.pdf) & 
 [inkscape_svg](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4_brackets.svg)  
 * supplemental figure 
  [pdf](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/supporting_information/LAR_orthogroup_selectionv1_guide_v5_SHaLRT_long_inpage_v3.pdf) & 
  [inkscape_svg](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/supporting_information/LAR_orthogroup_selectionv1_guide_v5_SHaLRT_long_inpage_v3.svg) 

Final alignment: [raw](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/alignments_raw/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi.fasta) 
& [trimmed](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/alignments_trimmed/1kP_LAR_selectionv1_guide_v5_aligned-mafft-linsi_trim-gt4-seq95-res7.fasta)

Final fasta used for alignment:
 * the [complete fasta](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/1kP_LAR_selectionv1_guide_v5.fasta) file
 * a [selection from the 1kP orthogroup](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/data/1kP_LAR_orthogroup_manual-selection-1.fasta) 
 * a manually composed set of [guide sequences](https://github.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/blob/main/data/Erbils_guide_v3.fasta) to annotate and interpret the tree.
 
### Figure as shown in Gungor et al. 2020 (in review) 
![PIP enzymes and LAR phylogenetic tree](https://raw.githubusercontent.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/main/figures/main_text/LAR_orthogroup_selectionv1_guide_v5_17cm_8pts_shalrt_circular_v4.1_brackets_600.svg.png)  

### Guide through the different folders and files.
The `data` folder contains (unaligned) fasta files, lists of sequence names, and aligned sequences in both trimmed and untrimmed versions. 
File names tend to be long, but are meant to reflect the history of that specific file. 
For example: `1kP_LAR_orthogroup_manual-selection-1_guidev4_aligned-mafft-linsi_trim-gt6-seq80.fasta` contains sequences from the 1kP LAR orthogroup from which a manual selection was taken. 
Second, a set of guide sequences (sequences whose function has been verified) was added.
These sequences were then aligned with mafft-linsi and trimmed with trimAL settings `-gt .6 and -seq 80.`

The `analyses` folder contains tree inferences. 
These are organised in folders of starting dataset, and then in folders of alignment and trimming strategy.
Still, a folder may contain several tree inferences made with IQTree. 
The final part of the filename sumarises the settings used to create a particular tree file. 
Note that intermediate trees are just that, intermediate results. 
The `fernLARclades_analyses` directory contains tree inferences on specifically the fern LAR, WLAR1 and WLAR2 clades as shown in figure 8 of Güngör _et al_. 2020.

The `figures` folder contains the final versions of the figures shown in Güngör _et al_. in several formats. 
These were made by importing a `.treefile` in [iToL](https://itol.embl.de/), then adding annotation manually, and downloading these as `.svg` file.
These `.svg` files were then finalised in inkscape to their published form and exported as pdf or png. 

The workflows for which data is shared here, are documented in JuPyter notebookbooks (`*.ipynb`).
The workflow describing the final version of the tree is [tree_building_workflow_v5](https://github.com/lauralwd/LAR_phylogeny_gungor-et-al-2020/blob/main/tree_building_workflow_v5.ipynb). 
The other two workflows are explorative and should be interpreted as such. 

### Data sources used in this project

