# A toy repo to play with Llama based on [MLX](https://github.com/ml-explore), Apple's own ML framework

## To start
When cloning this repo, also clone the submodule codellama by running
```bash
git submodule update --init --recursive
```

Request access to [Llama's weights](https://llama.meta.com/llama-downloads/). 

Then run `bash codellama/download.sh` to download weights.

I used weights `CodeLlama-7b` (13.49GB on disk)

Running 
```bash
python3 mlx-examples/llms/llama/convert.py --torch-path codellama/CodeLlama-7b -q
```
will create a new folder called `mlx_model` which stores the model weights (for 7b model weights is 3.8GB on disk)




## To run prmopt:
```bash
python3 mlx-examples/llms/llama/llama.py --prompt "hello"
```

--model-path <br />
Path to the model weights and tokenizer

--prompt <br />
The message to be processed by the model. Ignored when --few-shot is provided.

--few-shot <br />
Read a few shot prompt from a file (as in sample_prompt.txt).

--max-tokens <br />
How many tokens to generate

--write-every <br />
After how many tokens to detokenize

--temp <br />
The sampling temperature

--seed <br />
The PRNG seed


