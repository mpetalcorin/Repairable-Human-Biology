# Repairable Human Biology

A literature-informed computational proof of concept for modeling molecular repairability, closing repair windows, and age-associated decline.

## Overview

This repository presents a computational proof of concept for **Repairable Human Biology**, a framework that treats biological repairability as a measurable molecular state. Rather than focusing only on damage accumulation, the project asks whether ageing and chronic decline can be understood as the progressive loss of the body's ability to repair itself.

The repository contains a notebook that generates a synthetic, literature-informed dataset benchmarked to peer-reviewed  ageing and senescence literature. The notebook then performs descriptive analysis, state-space analysis, machine-learning prediction, and in silico intervention testing to explore whether repairability can be modeled as an integrated biological property.

## Core idea

The main hypothesis is that biological systems do not fail only because damage happens. They fail because, over time, they lose access to effective repair. In this project, that concept is represented as a latent variable called **repairability**, influenced by molecular features such as:

- reactive oxygen species, ROS
- ATP abundance
- electron transport chain, ETC, activity
- mtDNA copy index
- γH2AX DNA-damage burden
- IL-6 inflammatory signaling
- p16 and p21 senescence markers
- proteostasis capacity
- autophagy flux
- telomere length
- cytosolic mtDNA burden

## Repository structure

```
├── README.md
├── MODELCARD.md
├── DATASHEET.md
├── repairable_human_biology_poc.ipynb
└── repairable_human_biology_poc.html
```
##  What the notebook does

The notebook performs the following steps:
- 1.	Simulates a molecular dataset representing four biological states:
	•	young
	•	midlife
	•	older
	•	aged_stressed
- 2.	Benchmarks synthetic values to biologically plausible trends from literature on:
	•	hallmarks of ageing
	•	cellular senescence
	•	mitochondrial dysfunction
	•	oxidative stress
	•	proteostasis decline
	•	inflammatory mtDNA signaling
- 3.	Constructs:
	•	a continuous repairability score
	•	a binary repair_window_open variable
- 4.	Performs:
	•	descriptive analysis
	•	group-wise comparison
	•	correlation analysis
	•	principal component analysis, PCA
	•	k-means clustering
	•	random forest classification
	•	random forest regression
	•	in silico intervention simulation

##  Main outputs

The proof of concept generates:
	•	age-stratified boxplots and bar plots of molecular variables
	•	correlation heatmaps
	•	PCA state-space visualization
	•	unsupervised molecular state clusters
	•	feature importance plots for repair-window prediction
	•	observed versus predicted repairability plots
	•	intervention-effect plots across age groups

## Scientific framing

This project is based on the idea that ageing may be interpreted as a progressive narrowing of biological repair windows. In this framework, reversing aspects of ageing does not mean a vague return to youth. Instead, it means restoring specific maintenance functions that allow cells and tissues to remain recoverable, including:
	•	mitochondrial competence
	•	genome upkeep
	•	inflammatory control
	•	proteostasis
	•	autophagic quality control
	•	stress recovery capacity

## Important limitations

This repository is a proof of concept and not an experimental study.
- The dataset is synthetic.
- The repairability score is computationally constructed.
- The intervention effects are simulated predictions.
- The results should not be interpreted as clinical, diagnostic, or therapeutic claims.

The value of the repository lies in formalizing a new hypothesis in a transparent and testable way.

## How to run

Requirements

Recommended Python version:
	•	Python 3.10 or later

Suggested packages:
	•	numpy
	•	pandas
	•	matplotlib
	•	scikit-learn
	•	jupyter

## Install dependencies
```
pip install numpy pandas matplotlib scikit-learn jupyter
```
Example research questions supported by this repository
- Can repairability be represented as a molecular state?
- Which molecular variables best predict open versus closing repair windows?
- Does ageing-like decline emerge as a systems-level transition?
- Are coordinated rescue strategies predicted to outperform single-axis interventions?
- Can this framework guide future experimental studies in ageing, senescence, and resilience biology?

## Intended use

This repository is intended for:
	•	conceptual development of the Repairable Human Biology framework
	•	computational prototyping
	•	grant or programme concept support
	•	educational demonstration
	•	future extension into experimental design

It is not intended for:
	•	clinical decision-making
	•	patient diagnosis
	•	treatment recommendation
	•	direct biological inference without validation

## Future directions

Potential next steps include:
- validation in aged primary-cell datasets
- integration with real omics or imaging data
- organoid-based repair-window mapping
- perturbation modeling of rejuvenation strategies
- multimodal machine-learning models for repair-state prediction
- bounded intervention modeling for safe reopening of repair windows

## References

López-Otín, C., Blasco, M. A., Partridge, L., Serrano, M., & Kroemer, G. (2013). The hallmarks of aging. Cell, 153(6), 1194–1217. https://www.cell.com/cell/fulltext/S0092-8674(13)00645-4

López-Otín, C., Blasco, M. A., Partridge, L., Serrano, M., & Kroemer, G. (2023). Hallmarks of aging: An expanding universe. Cell, 186(2), 243–278. https://www.cell.com/cell/fulltext/S0092-8674(22)01377-0

Mapuskar, K. A., Flippo, K. H., Schoenfeld, J. D., et al. (2017). Mitochondrial superoxide increases age-associated susceptibility of human dermal fibroblasts to radiation and chemotherapy. Cancer Research, 77(18), 5054–5067. https://aacrjournals.org/cancerres/article/77/18/5054/618240/Mitochondrial-Superoxide-Increases-Age-Associated

Roger, L., Tomas, F., & Gire, V. (2021). Mechanisms and regulation of cellular senescence. International Journal of Molecular Sciences, 22(23), 13173. https://www.mdpi.com/1422-0067/22/23/13173

Victorelli, S., Douglass, S. M., Haley, K. J., et al. (2023). Apoptotic stress causes mtDNA release during senescence and drives the SASP. Nature, 622(7983), 627–636. https://www.nature.com/articles/s41586-023-06621-4

## Citation

**Petalcorin, M.I.R.** (2026). Repairable Human Biology. https://github.com/mpetalcorin/Repairable-Human-Biology
