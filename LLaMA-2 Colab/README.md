# Llama-2 Colab Notebook

This Colab notebook demonstrates how to use the Llama-2 language model with GPU acceleration using the `llama-cpp-python` package.

## Prerequisites

- Google Colab (or any Jupyter Notebook environment with GPU support)
- Hugging Face account (optional, required for downloading models from Hugging Face Hub)

## Installation

```python
# Install required packages
!CMAKE_ARGS="-DLLAMA_CUBLAS=on" FORCE_CMAKE=1 pip install llama-cpp-python==0.1.78 numpy==1.23.4 --force-reinstall --upgrade --no-cache-dir
!pip install huggingface_hub

# Import necessary modules
from huggingface_hub import hf_hub_download
from llama_cpp import Llama