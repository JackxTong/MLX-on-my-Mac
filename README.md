# A toy repo to play with Llama based on [MLX](https://github.com/ml-explore), Apple's own ML framework

## To run prmopt:
```bash
python3 mlx-examples/llms/llama/llama.py --prompt "hello"
```

## Options:
  
  --model-path
                        Path to the model weights and tokenizer
  
  --prompt      
                        The message to be processed by the model. Ignored when --few-shot is provided.
  
  --few-shot   
                        Read a few shot prompt from a file (as in `sample_prompt.txt`).
  
  --max-tokens
                        How many tokens to generate
  
  --write-every
                        After how many tokens to detokenize
  
  --temp          
                        The sampling temperature
  
  --seed         
                        The PRNG seed


## Weights
I used weights `codellama/CodeLlama-7b` from Meta's codellama repo.

Running 
```bash
python3 mlx-examples/llms/llama/convert.py --torch-path codellama/CodeLlama-7b -q
```
will create a new folder called `mlx_model` which stores the model weights (for 7b model weights is 3.8GB on disk)