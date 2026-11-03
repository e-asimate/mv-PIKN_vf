# Preprocessing and split provenance

This folder contains non-subject-specific configuration and provenance summaries for the CHB-MIT preprocessing run `run_20261028T165011846018Z`.

- `preprocessing_config.json`, `runtime_environment.json`, and `duplicate_channel_policy.json` record preprocessing parameters, package versions, and channel policy.
- `input_hashes.json` records SHA-256 fingerprints of the locked inputs used by the saved experiment plans.
- `scaler_hashes.json` records the three training-fitted scaler hashes used in the exploratory inner-fold comparison.

The full locked fold, seizure-event, inventory, and scaler artifacts are kept out of this public repository pending review of their subject-level content. The hash records let readers identify the exact artifacts without publishing their contents. EEG samples are not included.
