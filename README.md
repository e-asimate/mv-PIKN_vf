# mv-PIKN

Code and notebooks for a multi-view Koopman and Wilson–Cowan-inspired seizure-forecasting study using the CHB-MIT scalp EEG database. EEG data are not included; see [data/README.md](data/README.md).

## Repository status

The completed analysis currently reported here is an exploratory inner-validation comparison across three inner folds and two seeds. Its source is in the nested evaluation notebook; search for `short_three_model_mean_v1`. The redacted saved plans are in [configs/exploratory_three_model_mean_v1/](configs/exploratory_three_model_mean_v1/). The implementation hash in those plans was verified against the notebook’s embedded source.

The notebook also contains a distinct nested evaluation runner whose saved plan uses three epochs. That is separate from the 10,000-update exploratory comparison. The all-subject outer evaluation is incomplete, and the exploratory inner-validation findings should not be described as independent outer-test performance.

Notebook outputs were cleared before publication. EEG samples, model checkpoints, and prediction exports are not stored here.

## Workflow

1. Install packages in [requirements.txt](requirements.txt) and obtain CHB-MIT from PhysioNet.
2. Run [CHB_MIT_Preprocessing.ipynb](notebooks/01_preprocessing/CHB_MIT_Preprocessing.ipynb) to audit and preprocess the recordings.
3. Review and run the synthetic protocol checks in [CHB_MIT_Event_Scoring.ipynb](notebooks/02_scoring/CHB_MIT_Event_Scoring.ipynb).
4. Review [manifests/](manifests/) and [configs/](configs/) before running the nested evaluation notebook.
5. Use the latent notebooks under `notebooks/04_results_and_visualization/` to export and visualize latent representations. They require processed data, matching checkpoints, and latent exports, which are not stored here.

Notebooks under `notebooks/development/` are pilots and smoke tests, not substitutes for the full evaluation.

The results-plot notebook is not included because it bundles study-result data from private Drive; that data needs review before public release.

## Folders

- `notebooks/`: Colab notebooks grouped by workflow stage.
- `configs/`: saved settings and experiment provenance.
- `manifests/`: public-safe preprocessing configuration and hashed provenance summaries.
- `data/`: instructions only; no EEG data are included.
- `results/`: instructions only; no checkpoints or prediction exports are included.

## License

No reuse license has been selected yet.
