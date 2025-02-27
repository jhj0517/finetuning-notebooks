# Finetuning Notebooks

Notebooks to finetune several models that can run on Google Colab. 

## Notebooks

For the dataset sizes, usually 5 ~ 20 images are enough to train LoRAs.
<div align="center">

| Category                       | Model Type |                                                                                                       Notebook                                                                                                        |                                                                                                    Open in Colab                                                                                                     |
|--------------------------------|:---:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| **Flux**                       | LoRA | [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/flux/finetuning_notebooks_flux_lora_dreambooth.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/flux/finetuning_notebooks_flux_lora_dreambooth.ipynb) |
| **Hunyuan Video**              | LoRA |   [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/hunyuan/finetuning_notebooks_hunyuan_lora.ipynb)    |   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/hunyuan/finetuning_notebooks_hunyuan_lora.ipynb)    |
| **Wan Video**                  | LoRA |     [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/wan/finetuning_notebooks_wan_lora.ipynb)      |     [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/wan/finetuning_notebooks_wan_lora.ipynb)      |
| **SDXL**                       | LoRA | [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/sdxl/finetuning_notebooks_sdxl_lora_dreambooth.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/sdxl/finetuning_notebooks_sdxl_lora_dreambooth.ipynb) |
| **LTX Video**                  | LoRA |          [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/ltx/finetuning_notebooks_ltx_lora)           |       [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/ltx/finetuning_notebooks_ltx_lora.ipynb)        |
| **Diffusers Converter (Util)** | - | [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)](https://github.com/jhj0517/finetuning-notebooks/blob/master/utils/finetuning_notebooks_diffusers_converter.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhj0517/finetuning-notebooks/blob/master/utils/finetuning_notebooks_diffusers_converter.ipynb) |

</div>

## Tips
- [Preparing A Dataset with Captions](https://github.com/jhj0517/finetuning-notebooks/blob/master/docs/Preparing%20A%20Dataset%20with%20Captions.md)

## 🌺 Thanks

- Flux LoRA Training : https://github.com/ostris/ai-toolkit
- Hunyuan Video & Wan Video & LTX Video LoRA Training : https://github.com/tdrussell/diffusion-pipe
- Many training scripts are from the diffusers 🤗: https://github.com/huggingface/diffusers
