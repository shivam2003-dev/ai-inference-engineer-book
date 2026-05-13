# AI Inference Engineering Book

This repository contains the full LaTeX source for the book **AI Inference Engineering: Building Fast, Scalable, and Production-Ready AI Systems**.

## Overview

The book is a practical guide to modern LLM inference systems, from GPU fundamentals to production deployment. It covers:

- GPU architecture and CUDA foundations
- Transformer inference internals (prefill vs decode)
- KV cache design and memory management
- Quantization (FP8/INT4/FP4 tradeoffs)
- Speculative decoding and serving optimizations
- Runtime choices (vLLM, TensorRT-LLM, SGLang)
- Distributed inference patterns
- Monitoring, profiling, and Kubernetes deployment
- Reference appendices for CUDA, Linux operations, benchmarking, and profiling

Main source file:

- `book.tex`

## Compile TeX to PDF

### Prerequisites

- TeX distribution installed (recommended: TeX Live)
- `pdflatex` available in PATH
- `makeindex` available in PATH

### Build Commands

Run from the repository root:

```bash
pdflatex -interaction=nonstopmode -halt-on-error book.tex
makeindex book.idx
pdflatex -interaction=nonstopmode -halt-on-error book.tex
pdflatex -interaction=nonstopmode -halt-on-error book.tex
```

Output PDF:

- `book.pdf`

### Quick One-Command Build

```bash
pdflatex -interaction=nonstopmode -halt-on-error book.tex && \
makeindex book.idx && \
pdflatex -interaction=nonstopmode -halt-on-error book.tex && \
pdflatex -interaction=nonstopmode -halt-on-error book.tex
```