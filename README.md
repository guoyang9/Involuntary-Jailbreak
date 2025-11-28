# Involuntary Jailbreak

This is the official implementation for [Involuntary Jailbreak](https://arxiv.org/abs/2508.13246).

Implementing this method using APIs is quite simple and can be done in just a few steps. 

**Sucessfully tested LLMs**:
- **Google Gemini**
  - Gemini 3 Pro
  - Gemini 2.5 Pro, Gemini 2.5 Flash, Gemini 2.5 Flash Lite
  - Gemini 2.0 Flash
- **Anthropic Claude**
  - Sonnet 4.5, Sonnet 4
  - Opus 4.1, Opus 4
  - Sonnet 3.7
- **xAI Grok**
  - Grok 4.1, Grok 4
  - Grok 3, Grok 3 Fast, Grok 3 Mini
- **OpenAI**
  - GPT-4.1
  - GPT-4o
  - gpt-oss
- **Meta Llama**
  - Llama 4-Maverick-17B
  - Llama 3.1-405B, Llama 3.3-70B
- **DeepSeek**
  - DeepSeek R1
  - DeepSeek V3
- **Alibaba Qwen**
  - Qwen3-Coder-480B-A35B, Qwen3-235B-A22B
  - Qwen2.5-72B  

## Easy copy and test using [prompt](prompt.txt)
**Note**: My OpenAI account got banned due to successful trials, so please be careful when testing using chatGPT website (API should be fine).

## Disclaimer
The jailbreaking methods described in this paper are solely intended for responsible AI safety research and the development of more robust, secure AI systems.

### We aim to:
- Help researchers and developers identify vulnerabilities and strengthen defenses.
- Enable the AI community to proactively mitigate risks before malicious exploitation.
- Foster responsible innovation in AI security.

### We urge all readers and users to:
- Any misuse for harmful, unethical, or unauthorized purposes is strictly prohibited.
- Adhere to ethical guidelines and respect platform terms of service.
- Use this knowledge responsibly to advance safe and beneficial AI technologies.

## API batching
### Preparation
- Create a `api_key.py ` file under `tools`, and add your own api keys inside. 
- Some configs I leave to the [gen_config.yaml](gen_config.yaml) file.
- Note that I use together.ai to access open-sourced models, and you can also use your own API keys for other proprietary LLMs such as OpenAI GPT 4.1 and Grok 4.

### Generate responses
You should first take a look at the run_meta_prompt and uncomment the model that you want to test.
Otherwise some models may not work as expected.
```
python run_meta_prompt.py
```
### Judge using Llama Guard-4
I'm still using together.ai for this experiment.
```
python run_judge.py
```

## Citation
We appreciate your acknowledgement to our work by citing:
```bibtex
@misc{involuntary,
      title={Involuntary Jailbreak}, 
      author={Yangyang Guo and Yangyan Li and Mohan Kankanhalli},
      year={2025},
      eprint={2508.13246},
      archivePrefix={arXiv},
}
```

## Acknowledgement
We appreciate [together.ai](https://www.together.ai/) for providing us with the API access to open-sourced models.
For other proprietary LLMs such as OpenAI GPT 4.1 and Grok 4, please visit respective API website for more information.
