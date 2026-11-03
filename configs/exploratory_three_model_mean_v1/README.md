# Exploratory three-model comparison

The source code is in [CHB_MIT_Full_Nested_Evaluation_Final.ipynb](../../notebooks/03_training_and_evaluation/CHB_MIT_Full_Nested_Evaluation_Final.ipynb). Search the notebook for `short_three_model_mean_v1`. The implementation hash in the saved plans was verified against the notebook’s embedded implementation strings.

The redacted public plans summarize the two seeds (20261028 and 20261029) and three inner folds. They preserve the recorded training settings and hashes for the implementation, locked inputs, and training-fitted scalers, while omitting subject-level role assignments and checkpoint identifiers.

The comparison used 10,000 optimizer updates, batch size 24, learning rate 0.001, checkpoints every 250 updates, a 20% maximum warning-time constraint, and causal mean smoothing over the existing 75-window history (4 seconds per window). The recorded runtime was PyTorch 2.11.0+cu130 on a Tesla T4.

These are exploratory inner-validation analyses. Checkpoints and prediction exports are not included, so the public plans document configuration and provenance but do not alone reproduce the numerical results. The separate `nested_full_v1_1/experiment_plan.json` records a distinct three-epoch workflow.
