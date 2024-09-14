<h1 align="center"> CodeAttack 🧑‍💻🐞</h1> 
A novel jailbreak method CodeAttack to systematically investigate the safety vulnerability issues of LLMs in the domain of code. 
<br>   <br>

<h3 align="center">RESEARCH USE ONLY✅ NO MISUSE❌</h3>
<h3 align="center">LOVE💗 and Peace🌊</h3>

<p align="center" style="font-size:24px;"><b>CodeAttack is one of the strongest jailbreak methods for all LLMs so far.</b></p>

If you find a better method, please email me!

## 🆙 Updates
- An enhanced version of CodeAttack, highly effective against the latest `GPT-4` and `Claude-3` series models, will be available next week!

## 👉 Paper
For more details, please refer to our paper [ACL 2024](https://arxiv.org/abs/2403.07865).


## 🛠️ Usage
✨An example run:
```
python3 main.py --num-sample 1 \
--prompt-type python_stack_plus \ 
--query-file ./data/harmful_behaviors.csv \
--target-model=gpt-4o \
--judge \
--judge-model=gpt-4o \
--exp-name=main \
--target-max-n-tokens=1000 \
--multi-thread \
--temperature 0 \
--start-idx 0 --end-idx -1
```
### Experiments 
1. The 'data' foler contains the dataset `harmful_behaviors.csv` from [AdvBench](https://github.com/llm-attacks/llm-attacks). You can add your original dataset here.
2. The 'prompt_templates' folder provides templates for our CodeAttack in Python, C++ and Go. **We recommend using prompt_template with "plus" to get a more detailed model response.**
3. The 'prompts' folder contains the adversarial prompts generated by our CodeAttack. For convenience, we include three versions of CodeAttack curated using AdvBench: `data_python_string_full.json`, `data_python_list_full.json`, and `data_python_stack_full.json`.

## 💡Framework
<div align="center">
  <img src="figs/main.png" alt="Logo" width="500">
</div>


Overview of our CodeAttack. CodeAttack constructs a code template with three steps: (1) Input encoding which encodes the harmful text-based query with common data structures; (2) Task understanding which applies a decode() function to allow LLMs to extract the target task from various kinds of inputs; (3) Output specification which enables LLMs to fill the output structure with the user’s desired content.

## Citation

If you find our paper&tool interesting and useful, please feel free to give us a star and cite us through:
```bibtex
@inproceedings{
Ren2024codeattack,
title={Exploring Safety Generalization Challenges of Large Language Models via Code},
author={Qibing Ren and Chang Gao and Jing Shao and Junchi Yan and Xin Tan and Wai Lam and Lizhuang Ma},
booktitle={The 62nd Annual Meeting of the Association for Computational Linguistics},
year={2024},
url={https://arxiv.org/abs/2403.07865}
}

```