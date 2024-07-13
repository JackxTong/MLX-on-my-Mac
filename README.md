# A toy repo to play with Llama based on [MLX](https://github.com/ml-explore), Apple's own ML framework

## To run prmopt:
```bash
python3 mlx-examples/llms/llama/llama.py --prompt "hello"
```

## Options:

  -h, --help            show this help message and exit
  
  --model-path MODEL_PATH
                        Path to the model weights and tokenizer
  
  --prompt PROMPT       
                        The message to be processed by the model. Ignored when --few-shot is provided.
  
  --few-shot FEW_SHOT   
                        Read a few shot prompt from a file (as in `sample_prompt.txt`).
  
  --max-tokens MAX_TOKENS, -m MAX_TOKENS
                        How many tokens to generate
  
  --write-every WRITE_EVERY
                        After how many tokens to detokenize
  
  --temp TEMP           
                        The sampling temperature
  
  --seed SEED           
                        The PRNG seed


## Weights
I used weights `codellama/CodeLlama-7b` from Meta's codellama repo.

Running 
```bash
python3 mlx-examples/llms/llama/convert.py --torch-path codellama/CodeLlama-7b -q
```
will create a new folder called `mlx_model` which stores the model weights (for 7b model weights is 3.8GB on disk)