# Negative_CLIPort
## Problem Statement 
Most language-based models and datasets are developed in a positive tone biased dataset. We wanted to test and fine tune one such model for negative instructions for safety and security constraints.
Our approach: We took the fin-tuned CLIPort model and first tested the model by modifying the instructions with a negative tone like “Pick up the green block that’s not in the yellow square” and tested it. The model failed at Zero shot testing. Hence, we created a new negative dataset to conform to this requirement.
## Summary:
Initially to test Zero-shot capability we changed the prompt for certain tasks with a negative tone.
The model failed Zero-shot testing hence we decided to work on fine-tuning the model with those negative prompts.
We created actuation image data in the standard way but changed the prompts, for example “Place the block in the square that’s blue” was changed to “Place the block in the square that’s not red” given red in in the environment.
This dataset is loaded, and the model was fine-tuned to negative instructions.
## Outcome
We obtained 93% accuracy after training over 20 epochs but observed some jitter while performing the action.
Reference: https://cliport.github.io/


