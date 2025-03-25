---
title: Fast3R 复现笔记
published: 2025-03-25
description: '根据Github开源的Fast3R代码，从数据准备开始跑通Fast3R的训练流程。'
image: ''
tags: ['Fast3R', 'AI']
category: '笔记'
draft: true 
lang: 'zh-CN'
---

## 1. 代码准备
Fast3R 的代码库是 [https://github.com/facebookresearch/fast3r](https://github.com/facebookresearch/fast3r)，可以直接根据官方Installaton 中的指引进行安装。

```bash
# clone project
git clone https://github.com/facebookresearch/fast3r
cd fast3r

conda create -n fast3r python=3.11 cmake=3.14.0 -y
conda activate fast3r

# install PyTorch (adjust cuda version according to your system) 这里安装PyTorch, 我直接pip安装了2.6.0版本
# conda install pytorch torchvision torchaudio pytorch-cuda=12.4 nvidia/label/cuda-12.4.0::cuda-toolkit -c pytorch -c nvidia
pip3 install torch torchvision torchaudio

# install PyTorch3D from source (the compilation will take a while)
pip install "git+https://github.com/facebookresearch/pytorch3d.git@stable"

# install requirements
pip install -r requirements.txt

# install fast3r as a package (so you can import fast3r and use it in your own project)
pip install -e .
```

## 2. 测试运行


## 3. 数据准备
### 3.1 Co3d


