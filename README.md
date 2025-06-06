# Vision Transformers for Single Image Dehazing

> **Abstract:** 
With the extensive application of satellite remote sensing technologies in environmental monitoring and other fields, haze-induced image degradation has become a critical bottleneck for quantitative remote sensing analysis.Although convolutional neural networks  dominate current research in Remote Sensing Dehazing, their inherent local receptive field characteristics result in insufficient global contextual modeling capabilities, severely limiting the upper performance boundaries of existing models. While traditional Transformer architectures possess global modeling capabilities, they suffer from quadratic computational complexity bottlenecks when processing high-resolution images, hindering practical applications. To address the aforementioned challenges, this paper proposes a novel diffused attention mechanism that enables efficient global feature modeling while reducing computational costs. Specifically, this study employs a window-based Transformer architecture with the following innovative designs to enhance feature representation: First, a sub-block partitioning strategy is implemented within local windows, enforcing a homogeneous attention weight allocation mechanism for isomorphic sub-blocks. Subsequently, a multi-level clarity fusion module (Clarity Mixing, CMix) is proposed, constructing a multi-scale convolutional parallel architecture to mitigate weakened intra-block information interaction. Simultaneously, Snake-Scan Block Displacement is applied to reorganize image blocks without disrupting spatial continuity, thereby strengthening inter-window information connectivity. Experimental results demonstrate that this method achieves state-of-the-art performance on the RICE dataset, exceeding 36dB in peak signal-to-noise ratio (PSNR). Notably, compared with standard Transformer architectures, our model maintains superior restoration quality while achieving multiple times faster training speed. These breakthroughs provide novel technical pathways for efficient global modeling in image restoration tasks.In addition, we collected a large-scale non-uniform remote sensing dehazing dataset RSHaze5K for evaluating the dehazing capability of networks on heterogeneous images.

![network](https://github.com/liunanwangxing/Winscaleformer/blob/main/network.jpg)

## Preparation

### Install

We test the code on PyTorch 1.10.2 + CUDA 11.3 + cuDNN 8.2.0

### Download

You can download the pretrained models and datasets on  [BaiduPan](https://pan.baidu.com/s/1WVdNccqDMnJ5k5Q__Y2dsg?pwd=gtuw) ().

Currently, we only provide RSHaze5K dataset.

The final file path should be the same as the following:

```
RSHaze5K
  ├─ train
  │   ├─ clear
  │   │   └─ ... (image filename)
  │   └─ hazy
  │       └─ ... (corresponds to the former)
  └─ test
  └─ ...
   
```
