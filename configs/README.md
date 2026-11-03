# Configurations

- `nested_full_v1_1/experiment_plan.json` records the separate nested evaluation runner plan saved in Drive. It uses three epochs and is not the 10,000-update exploratory comparison.
- `exploratory_three_model_mean_v1/` contains redacted public plan summaries for the two-seed, three-inner-fold comparison. The exact source code is in the nested evaluation notebook and is identified there by `short_three_model_mean_v1`.

The public plan summaries retain model training settings and input/scaler hashes. Subject-level roles and checkpoint identifiers are omitted. Checkpoints and prediction outputs are not included. The full 23-outer-fold evaluation was not completed.
