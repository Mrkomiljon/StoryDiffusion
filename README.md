

<div align="center">
  
## StoryDiffusion: Consistent Self-Attention for Long-Range Image and Video Generation  [![Paper page](https://huggingface.co/datasets/huggingface/badges/resolve/main/paper-page-md-dark.svg)]()
[[Paper](https://arxiv.org/abs/2405.01434)] &emsp; [[Project Page](https://storydiffusion.github.io/)] &emsp;  [[🤗 Comic Generation Demo ](https://huggingface.co/spaces/YupengZhou/StoryDiffusion)] [![Replicate](https://replicate.com/cjwbw/StoryDiffusion/badge)](https://replicate.com/cjwbw/StoryDiffusion) <br>


</div>

<div align="left">
  
  #### For results sharing and discussion: https://discord.gg/hSJZ35fV
  #### For codebase and deployment-related discussion: https://discord.gg/2HFUHT9p
</div>

---

Official implementation of **[StoryDiffusion: Consistent Self-Attention for Long-Range Image and Video Generation]()**.






### 🌠  **Key Features:**
StoryDiffusion can create a magic story by generating consistent images and videos. Our work mainly has two parts: 
1. Consistent self-attention for character-consistent image generation over long-range sequences. It is hot-pluggable and compatible with all SD1.5 and SDXL-based image diffusion models. For the current implementation, the user needs to provide at least 3 text prompts for the consistent self-attention module. We recommend at least 5 - 6 text prompts for better layout arrangement.
2. Motion predictor for long-range video generation, which predicts motion between Condition Images in a compressed image semantic space, achieving larger motion prediction. 

## 🔥 **Ref image**
![11](https://github.com/Mrkomiljon/StoryDiffusion/assets/92161283/94cd32fe-69f7-48a1-850b-4f69ef267d47)

## 🔥 **Negative_prompt** 
**"In a quaint old house, a man discovers a newspaper article about a hidden treasure in the nearby forest. Driven by dreams of fortune, he drives alone along a deserted road leading into the dark woods. As night falls, a sudden encounter with a wild tiger heightens the peril. Startled and fearful, he flees deeper into the forest, where he stumbles upon an ancient, secluded treasure house. Inside, surrounded by untold riches and no sign of the modern world, his laughter echoes, a sound of pure joy and triumph over his earlier fears."**

## 🔥 **Comic Description (each line corresponds to a frame).** 

**At home, reading a newspaper - #At home, the newspaper reveals there's a hidden treasure in the nearby forest.
- On the road, approaching the forest - #He drives to the forest, fueled by dreams of discovering the hidden treasure.
- Encounter in the forest at night - #A tiger suddenly appears on the path, its eyes glowing in the dark forest at night.
- Frightened in the forest at night - #Startled and very frightened, he opens his mouth in shock, standing frozen in the forest at night.
- Running through the forest at night - #In a panic, he runs very fast through the dark forest, trying to escape the looming shadows and eerie sounds.
- Discovery of the house in the forest at night - #As he stumbles through the darkness, he suddenly discovers the treasure house hidden amongst the trees!
**

### Comics generation 


<img width="1151" alt="image" src="https://github.com/Mrkomiljon/StoryDiffusion/assets/92161283/1292b4dc-0257-44c6-ad96-2166c0ee7b86">



---

# 🔧 Dependencies and Installation

- Python >= 3.8 (Recommend to use [Anaconda](https://www.anaconda.com/download/#linux) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html))
- [PyTorch >= 2.0.0](https://pytorch.org/)
```bash
conda create --name storydiffusion python=3.10
conda activate storydiffusion
pip install -U pip

# Install requirements
pip install -r requirements.txt
```
# How to use

Currently, we provide two ways for you to generate comics.

## Use the jupyter notebook

You can open the `Comic_Generation.ipynb` and run the code.

## Start a local gradio demo
Run the following command:

```python
python gradio_app_sdxl_specific_id.py
```

We provide a low GPU Memory cost version, it was test on a machine with 24GB GPU-memory(Tesla A10) and 30GB RAM, and expcted work well with >20 G GPU-memory.

```python
python gradio_app_sdxl_specific_id_low_vram.py
```



```BibTeX
@article{Zhou2024storydiffusion,
  title={StoryDiffusion: Consistent Self-Attention for Long-Range Image and Video Generation},
  author={Zhou, Yupeng and Zhou, Daquan and Cheng, Ming-Ming and Feng, Jiashi and Hou, Qibin},
  year={2024}
}
