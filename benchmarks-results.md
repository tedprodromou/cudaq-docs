# cudaq-docs Documentation Usage Test Results

Test notes for LLM-automated CUDA-Q Python code generation, showing improvement using llms.txt and cuda-q skills. Tests were run on Google Colab in October 2026, running Gemini 3.5 Flash with NVIDIA CUDA-Q for quantum simulation.

Ran tests to generate Python scripts based on common quantum computing tasks, with 15 prompts given beforehand. Ran test series three times, once with only cuda-q loaded, once with llms.txt additionally loaded, and once with cudaq-guide additionally loaded.

## Results

* Without llms.txt or skills: 3 passed without errors, 8 passed after errors, 3 never passed. Average 1.8 errors per completed task.
* With llms.txt: 7 passed without errors, 5 passed after errors, 2 never passed. Average 1.5 errors per completed task.
* With llms.txt and cudaq-guide skill: 6 passed without errors, 5 passed after errors, 3 never passed. Average 1.45 errors per completed task.

Using llms.txt unambiguously improved results, with 1 more test passed, 4 more tests passed without errors, and fewer errors per task.

Using the cudaq-guide skills as well as llms.txt was more ambiguous, with fewer tests passed overally but even lower errors per task.

Specifically, the cudaq-guide skill had problems understanding when to use the cudaq.sample versus cudaq.run method and difficulty with variational optimization. However, the cudaq-guide skill was needed to prepare code for real Quantinuum hardware.

## Conclusions

The cudaq-guide skill could be improved by adding both positive and plausible negative examples of using conditional logic and variational optimization.

## Data Sources

[CUDAQ Benchmark - No Skills.ipynb](https://colab.research.google.com/drive/1BGiSE8UL96q9T4uXFlQWXcMiFhod0ive?usp=sharing)
[CUDAQ Benchmark - llmstxt.ipynb](https://colab.research.google.com/drive/1vsoXVAv9-F4W63m7APkWe45Og5eV97V1?usp=sharing)
[CUDAQ Benchmark - cudaqguide.ipynb](https://colab.research.google.com/drive/1pEZ5uq1u8IJPSpLxSkTT_UQ5skspyibd?usp=sharing)
[CUDA-Q Script Test Matrix (Google Spreadsheet)](https://docs.google.com/spreadsheets/d/13ViB_eKbL3Dr6iy9VP4_WvjlKQV41VQPCtE4-x6D-Vk/edit?usp=sharing)
