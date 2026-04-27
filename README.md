# Metabarcoding_ReferenceDatabase



## Description

This repository contains the reference databases used for the taxonomic assignment of DNA metabarcoding data. 
We created two reference databases for two specific regions, the Belgian Part of the North Sea (BPNS) and the area where the Belgian fishing fleet is active (BeFishingFleet) which contains reference sequences for species occurring in Belgium, the United Kingdom and the Netherlands. For each region a reference database was create for fish (Fish) and invertebrate (Inv)species.
At the end of each year the reference databases will be updated.

## Map order

* assets\
Contains the reference databases and is subdivided by region (BPNS, BeFishingFleet) and each region is subdevided by taxonomic group (Fish, Inv)\
Each subfolder contains:\
    * Exclusion file:\
    containing sequences that were flagged as misannotated
    *  Species-table file:\
    Containing the species names and their synonyms known to occur in the region of interest
    * Species-habitat file:\
    Containing the species list and the habitat (Brackish, Marine) they occur in
    * Taxonomy-changes file:\
    Containing a list of species names that are addjusted to be able to run the scripts correctly
    * Folder fasta:\
    Containing the reference database in different formats:\
        * csv
        * dada2
        * qiime2
        * sintax
* reports\
Contains the reports on how each reference database was created and the stats files containing detailed information about the database version.

## Information on the database creation
These reference databases were created using the [meta-fish-lib pipeline](https://github.com/genner-lab/meta-fish-lib) with some adjustments included.\
To create the species list we used a combination of FishBase (Fish) or SeaLifeBase (Inv), and the long-term trawl- and grab-data available at ILVO, and WoRMS to assure the correct scientific name. For the invertebrates species list, WoRMS was also used to add the synonyms from invertebrates that were present in the ILVO database but that were unavailable in SeaLifeBase.\
The Exclusion file was not created manually but was created using a combination of [SATIVA](https://github.com/amkozlov/sativa?tab=readme-ov-file) and BLASTn results. 
