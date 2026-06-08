# medicinal-plant-open-data-framework
Leakage-aware open-data framework integrating genomic, biosynthetic, soil, climate, and occurrence evidence for medicinal plant metabolite research.
# Integrating biosynthetic, genomic and ecological open data for medicinal plant metabolite research

This repository contains the data-science workflow supporting the project:

**Integrating biosynthetic, genomic and ecological open data for medicinal plant metabolite research: a leakage-aware data-science framework**

The project develops a reproducible open-data framework for medicinal plant metabolite research. It integrates biosynthetic-pathway evidence, genetic-resource availability, taxon–compound annotations, GBIF occurrence records, SoilGrids soil variables, and NASA POWER climate features into interpretable evidence profiles and validation-aware machine-learning analyses.

The framework is designed for cases where new laboratory genomic, transcriptomic, or metabolomic data are not available, but public biological and ecological repositories can be used to support transparent hypothesis generation and experimental planning.

## Scientific aim

Medicinal plant metabolite research increasingly depends on heterogeneous public data. Relevant evidence is distributed across sequence databases, protein repositories, pathway resources, biodiversity occurrence records, soil layers, climate products, and literature-derived compound annotations.

This project provides a structured workflow for integrating those evidence layers while avoiding unsupported claims. The framework distinguishes between:

- biosynthetic and pathway evidence, used to support taxon–compound plausibility;
- genetic-resource evidence, used to describe public sequencing and annotation readiness;
- occurrence, soil, and climate evidence, used to characterize ecological niche context;
- machine-learning scores, interpreted as ranking or prioritization outputs;
- negative-control analyses, used to define what the open data do not support.

The outputs should be interpreted as evidence-weighted hypotheses for future experimental work, not as confirmed metabolite detections or metabolite-concentration predictions.

## Case-study taxa

The main medicinal plant taxa included in the workflow are:

- *Artemisia annua*
- *Glycyrrhiza glabra*
- *Hypericum*
- *Rhodiola*
- *Sedum*
- *Taxus*

Additional family-level records are used in the genetic/pathway branch as hierarchical or background context.

## Target compounds and compound classes

The compound targets and compound classes include:

- artemisinin
- glycyrrhizin
- hypericin
- salidroside
- tyrosol
- paclitaxel
- flavonoids
- phenolic compounds
- alkaloids
- terpenoids

Specific molecular compounds and broad compound classes are handled separately because they represent different levels of biological specificity.

## Open data sources

The workflow uses public biological and ecological resources, including:

- NCBI Taxonomy
- NCBI Nucleotide
- NCBI Assembly
- NCBI Protein
- ENA sequencing metadata
- UniProt
- KEGG
- PubMed
- PubChem
- GBIF
- SoilGrids
- NASA POWER

The workflow is metadata-first and avoids unnecessary large-scale downloads by default. API responses and intermediate tables are cached where possible to improve reproducibility and reduce repeated remote requests.

## Repository structure

Recommended repository organization:

```text
medicinal-plant-open-data-framework/
├── README.md
├── LICENSE
├── CITATION.cff
├── notebooks/
│   ├── notebook1_gen_data_collection.ipynb
│   ├── notebook2_gen_data_analysis.ipynb
│   ├── notebook3_gen_data_modelling.ipynb
│   ├── notebook1_soil_data_collection.ipynb
│   ├── notebook2_soil_data_analysis.ipynb
│   ├── notebook3_soil_data_modelling.ipynb
│   ├── notebook1_climate_data_collection.ipynb
│   ├── notebook2_climate_data_analysis.ipynb
│   └── notebook3_climate_data_modelling.ipynb
├── data/
├── derived/
├── figures/
├── outputs/
└── manuscript/
