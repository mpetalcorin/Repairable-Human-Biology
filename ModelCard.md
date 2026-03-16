# Model Card

## Model name

Repairable Human Biology proof-of-concept models

## Model version

Version 1.0

## Model type

This repository contains two supervised machine-learning models:

1. **Random forest classifier**
   - predicts whether a simulated biological sample has an **open repair window** or a **closing/closed repair window**

2. **Random forest regressor**
   - predicts a continuous **repairability score**

These models are trained on a synthetic, literature-informed molecular dataset.

## Summary

The models are designed as proof-of-concept tools to test whether integrated molecular variables can be used to represent and predict biological repairability. They are not intended for clinical use and should not be interpreted as validated biological instruments.

## Intended use

### Appropriate use

These models are intended for:

- conceptual exploration of repairability as a systems property
- hypothesis generation
- methodological demonstration
- educational use
- programme or grant development
- benchmarking analysis pipelines for future real-world datasets

### Inappropriate use

These models must not be used for:

- medical diagnosis
- patient stratification
- treatment selection
- clinical prognosis
- commercial health claims
- claims of biological rejuvenation or anti-ageing efficacy

## Training data

The training data are **synthetic**. They were generated using literature-informed directional trends and representative ranges derived from peer-reviewed studies on:

- ageing hallmarks
- cellular senescence
- mitochondrial dysfunction
- oxidative stress
- proteostasis decline
- inflammatory mtDNA signaling

No real patient-level or experimental sample-level data were used.

## Input features

The models use the following features:

- age_years
- ros_fold_vs_young
- atp_au
- etc_activity_pct
- mtdna_copy_index
- gammaH2AX_foci
- IL6_pg_ml_index
- p16_expr_fold
- p21_expr_fold
- proteostasis_pct
- autophagy_flux_pct
- telomere_kbp
- cytosolic_mtDNA_fold

## Output targets

### Classifier target
- `repair_window_open`
  - 1 = repair window open
  - 0 = repair window closing or closed

### Regressor target
- `repairability_score`
  - continuous latent variable representing the degree of biological repair competence

## Model architecture

### Classifier
- algorithm: RandomForestClassifier
- trees: 400
- maximum depth: constrained
- leaf size: constrained for regularization

### Regressor
- algorithm: RandomForestRegressor
- trees: 400
- maximum depth: constrained
- leaf size: constrained for regularization

## Performance

Because the dataset is synthetic, performance metrics reflect **internal consistency within the simulated framework**, not real-world generalization.

Reported metrics in the notebook include:

### Classifier
- area under the ROC curve, AUC
- accuracy
- classification report

### Regressor
- R²
- root mean squared error, RMSE
- permutation feature importance

These metrics should be interpreted as proof-of-concept indicators only.

## Factors influencing performance

Performance depends on:

- how the synthetic data were generated
- the weights used to define the latent repairability score
- the amount of simulated noise
- the chosen feature distributions
- the age-group and tissue modifiers

The models may perform very differently on real experimental data.

## Biological interpretation

The models operationalize the idea that repairability emerges from the interaction of:

- oxidative stress
- energy metabolism
- DNA-damage burden
- senescence-marker expression
- inflammatory reinforcement
- proteostasis
- autophagic capacity
- telomere integrity
- mtDNA-linked distress signaling

In this framework, higher repairability is associated with:
- lower ROS
- lower γH2AX
- lower IL-6
- lower p16 and p21
- higher ATP
- higher ETC activity
- stronger proteostasis
- stronger autophagy
- longer telomeres

## Ethical considerations

These models concern ageing, resilience, and repair biology, all of which can easily be overinterpreted. Care must therefore be taken not to misrepresent this repository as evidence of a validated rejuvenation technology.

Key ethical cautions include:

- synthetic data do not justify clinical claims
- biological ageing is heterogeneous and context-dependent
- real interventions aimed at reopening repair windows may carry risks, including cancer promotion if cellular plasticity is unsafely manipulated
- computational proxies for repairability may overlook important tissue-specific and organism-level factors

## Limitations

- The dataset is fully synthetic.
- The target score is model-defined, not experimentally measured.
- The models are not externally validated.
- No causal inference is established.
- Tissue contexts are simplified.
- Intervention simulations are heuristic and not pharmacological models.

## Recommendations for future model development

Future versions should include:

- real longitudinal omics datasets
- experimental perturbation data
- external validation cohorts
- interpretable causal models
- uncertainty estimation
- safer biological constraints
- multi-omics integration
- tissue-specific repairability models

## Citation

**Petalcorin, M.I.R.** (2026). Repairable Human Biology proof-of-concept models. https://github.com/mpetalcorin/Repairable-Human-Biology
