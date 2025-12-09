## HW11 - Code Interpretability Question Refactor

# Setup Instructions 

Open the notebook in Google Colab:

Upload q_hand_transformer.ipynb to Google Colab, or
Use the "File" → "Upload notebook" option in Colab
Run all cells sequentially (Cell → Run All)

Note: A GPU is not necessary for this task. If you're using Colab, you can select "Runtime" → "Change runtime type" and choose "None" as the hardware accelerator.

# Updates

1. Debugging Features:
- Added the function `plot_weight_heatmap` which provides the ability to visualize the weights of the matrices being designed.
- For `single_attention_head` and `induction_copy_head` the `debug` parameter was added which enables visualizations for important matrices and attention outputs.

2. Improved Readability:
- All constants are now in uppercase (SEED, EPS)
- Changed variable names in `single_attention_head`: 
    - `Z` -> `scores`
    - Created `masked_scores` instead of just updating `Z`
    - `e_Z` -> `exp_scores`
    - `attn_scores` -> `attn_weights`
    - `XOV` -> `projected_values`
- Changed variable names in `induction_copy_head`:
    - 

3. Cleaned Testing Code:
- `pathlib` is being used for file paths
- Using `.items()` to iterate over the test case dictionary instead of 

4. Standardized Formatting:
- Using 4 spaces for all indentation
- Added type hinting to all functions