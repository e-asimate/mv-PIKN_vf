# mv-PIKN

Code and notebooks for the multi-view Koopman and Wilson–Cowan-inspired seizure-forecasting study using the CHB-MIT scalp EEG database. The dataset itself is not included; see [`data/README.md`](data/README.md).

## Repository status

This repository organizes the current preprocessing, scoring, evaluation, and analysis notebooks. The `CHB_MIT_Full_Nested_Evaluation_Final.ipynb` file is a planned evaluation workflow: its saved configuration uses three balanced epochs, defaults to `outer_chb01` and seed `20261028`, and has no recorded execution counts. It should not be cited as the exact source of previously reported 10,000-update exploratory results unless its code and settings are reconciled with the run that generated those results. The study remains exploratory; the planned all-subject outer evaluation is not complete.

Notebook outputs were cleared to keep the repository focused on source and avoid committing cached run output. The notebook code and explanatory text were retained.

## Workflow

1. Install the packages in [`requirements.txt`](requirements.txt) and obtain CHB-MIT from PhysioNet.
2. Run [`CHB_MIT_Preprocessing.ipynb`](notebooks/01_preprocessing/CHB_MIT_Preprocessing.ipynb) to audit and preprocess the recordings and create fold-specific scaling artifacts.
3. Review and run the synthetic protocol checks in [`CHB_MIT_Event_Scoring.ipynb`](notebooks/02_scoring/CHB_MIT_Event_Scoring.ipynb).
4. Review the fixed plan and paths before enabling training in [`CHB_MIT_Full_Nested_Evaluation_Final.ipynb`](notebooks/03_training_and_evaluation/CHB_MIT_Full_Nested_Evaluation_Final.ipynb). Its current default is one outer fold and one seed, not the complete planned study.
5. Use the latent notebooks under `notebooks/04_results_and_visualization/` to export and visualize latent representations. They require processed data, checkpoints, and latent exports, which are not stored here. The results-plot notebook is not included yet because it bundles study-result data; review that data for public release before adding the notebook.

The notebooks under `notebooks/development/` are smoke tests and development pilots. They are not substitutes for the full evaluation.

## Folders

- `notebooks/`: runnable Colab notebooks, grouped by workflow stage.
- `configs/`: location for frozen run configurations and software provenance.
- `manifests/`: location for reviewed fold and event manifests; none are included yet.
- `data/`: instructions only; no EEG data are included.
- `results/`: instructions only; no checkpoints, predictions, or generated run outputs are included.

## License

No reuse license has been selected yet. A license should be added after the project authors agree on the terms.
