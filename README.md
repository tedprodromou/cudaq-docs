# cudaq-docs

[CUDA-Q](https://developer.nvidia.com/cuda-q) streamlines hybrid application development and promotes productivity and scalability in quantum computing. It offers a hybrid programming model designed for a setting where CPUs, GPUs, and QPUs work together. CUDA-Q contains support for programming in Python and in C++.

As an attempt to improve performance for CUDA-Q users, I ran benchmarks to identify problem areas, revised the llms.txt for improved effectiveness, and measured improvements against the listed benchmarks.

[llms.txt](llms.txt) is the revised version of llms.txt, organized by how an LLM would use the documentation for CUDA-Q, with examples (links to documentation) added for some common pitfalls.

## Revisions to llms.txt

The [original llms.txt](llms-old.txt) (the previous version) was a simple table of contents of the CUDA-Q documentation site. I revised it in two ways:

- **Organized by use.** Sections are grouped by how people use them: getting started, the API, using CUDA-Q, and examples. For example, Installation moved from Optional into Using CUDA-Q.
- **Examples for common errors.** Added direct links to pages covering the mistakes LLMs made most often in the benchmarks: when to use `cudaq.sample` versus `cudaq.run`, noisy simulation, and computing expectation values.

[Benchmark Results](benchmark-results.md) compares LLM code generation with no documentation loaded, with llms.txt, with llms.txt plus the [cudaq-guide skill](https://www.skills.sh/nvidia/cuda-quantum/cudaq-guide), and with the revised llms.txt.