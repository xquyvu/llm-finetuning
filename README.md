# LLM fine tuning

Prepare data and fine-tune a language model.

Credits to deeplearning.ai for the original learning material.

## Notebooks

[Why finetuning](01_why_finetuning.ipynb): Explains the importance of fine tuning language models. This compared the performance of 2 versions of Alpaca-7b, before and after fine tuning for conversation.

[Where finetuning fits in](02_where_finetuning_fits_in.ipynb): Compares fine tuning and pretraining. Pre-training is useful for developing a general purpose language model, and establish a foundating for fine tuning. Fine-tuning is considered the next stage, where we develop a model for a specific task. I explored 2 ways of structuring the data for fine tuning.

[Instruction tuning](03_instruction_tuning.ipynb): Compares the performance of 2 versions of Alpaca-7b and pythia-70m, before and after fine tuning for instruction following. ChatGPT is still the best model for instruction following. I couldn't run the notebook locally because it requires a token for Lamini.

[Data preparation](04_data_preparation.ipynb): Prepares the data for finetuning language model for instruction following. I went through the basic steps of tokenization, padding + truncating and finally, train-test split.

[Fine tuning](05_finetuning.ipynb): Finetuned a `pythia-70m` model for instruction following. The result was pretty bad, as expected. I then tried a fully fine-tuned `pythia-70m` model which was much better.

[Evaluation](06_evaluation.ipynb): Evaluate the LM on the ARC benchmark, using the `lm-evaluation-harness` package. The fine-tuned model performed worse than the original one. This is expected because the the orignal model is a general purpose language model, while the fine-tuned model was tuned based on a task that's different from the benchmark! However the spirit is to experiment with the evaluation process.
