# RenderMe-360 Dataset
[![arXiv](https://img.shields.io/badge/arXiv-xxxx.xxxxx-b31b1b.svg)]() <a href="https://renderme-360.github.io/">
<img alt="Project" src="https://img.shields.io/badge/-Project%20Page-lightgrey?logo=Google%20Chrome&color=informational&logoColor=white"></a> 
<a href="https://youtu.be/ZtlxiMeGOoM"><img alt="Demo" src="https://img.shields.io/badge/-Demo-ea3323?logo=youtube"></a> 

This is the Benchmark PyTorch implementation of the paper *"[RenderMe-360: Large Digital Asset Library and Benchmark Towards High-fidelity Head Avatars]()"*.

<img src="./docs/teaser.png" width="96%" height="96%">

<img src="./docs/teaser1.gif" width="96%" height="96%">

> 
>
> **Abstract:** *Synthesizing high-fidelity head avatars is a central problem for many applications on AR, VR, and Metaverse. While head avatar synthesis algorithms have advanced rapidly, the best ones still face great obstacles in real-world scenarios. One of the vital causes is the inadequate datasets  -- 1) current public datasets can only support researchers to explore high-fidelity head avatars in one or two task directions, such as viewpoint, head pose, hairstyle, or facial expression; 2) these datasets usually contain digital head assets with limited data volume, and narrow distribution over different attributes, such as expressions, ages, and accessories. In this paper, we present {\textbf{RenderMe-360}}, a comprehensive 4D human head dataset to drive advance in head avatar algorithms across different scenarios. RenderMe-360 contains massive data assets, with 250+ million complete head frames and over 800k video sequences from 500 different identities captured by synchronized HD multi-view cameras at 30 fps. It is a large-scale digital library for head avatars with three key attributes: 1) High Fidelity: all subjects are captured by 60 synchronized, high-resolution 2K cameras to collect their portrait data in 360 degrees. 2) High Diversity: The collected subjects vary from different ages, eras, ethnicity, and cultures, providing abundant materials with distinctive styles in appearance and geometry. Moreover, each subject is asked to perform various dynamic motions, such as expressions and head rotations, which further extend the richness of assets. 3) Rich Annotations: the dataset provides annotations with different granularities: cameras' parameters, background matting, scan, 2D as well as 3D facial landmarks, FLAME fitting labeled by semi-auto annotation, and text description.
Based on the dataset, we build a comprehensive benchmark for head avatar research, with 16 state-of-the-art methods performed on five main tasks: novel view synthesis, novel expression synthesis, hair rendering, hair editing, and talking head generation. Our experiments uncover the strengths and weaknesses of state-of-the-art methods, showing that extra efforts are needed for them to perform in such diverse scenarios. RenderMe-360 opens the door for future exploration in modern head avatars. All of the data, code, and models will be publicly available at https://renderme-360.github.io/.* <br>

## Updates

- 2023.05.09: Technical report, dataset and code will be released in May.
- 2023.05.08: The project page is created.


## Contents
1. [Features](#features)
2. [Data Download](#Data-Download)
3. [Benchmark & Model Zoo](#Benchmark-&-Model-Zoo)
4. [Usage](#Usage)
5. [Related Works](#Related-Works)
6. [Citation](#citation)
6. [Acknowlegement](#Acknowlegement)


# Features
*  High Fidelity: Build a multi-video camera capture cylinder called POLICY to capture synchronized multi-view videos. 60 instructive cameras / 2448 × 2048 / 30FPS for video capture. 
* High Diversity: RenderMe-360 is a large scale dataset with 500 IDs and 243M frames in total, far exceeds other datasets. A wide diversity including era, ethnicity, accessory and makeup. Each subject capture about 20-30 performance parts in cluding expression, hair, and speech.
* Rich Annotations: Rich and multimodal annotation far beyond other datasets: face landmark 2d & 3d, front-back matting, FLAME parameters, scan mesh, uv map, action units, appearance annotation and text description. 
## Data Download
The dataset will be released in May.

## Benchmark & Model Zoo

We provide for each benchmark the pretrained model, code for training & evaluation reimplementation, and dataset for training.

| Benchmark                          | Aspect                           | Pretrained Model                                                | Reimplementation                    | Dataset      |
| ------------------------------- | ------------------------------- | ------------------------------------------------------------ | ---------------- | -------------------------------------------- |
| instant-ngp   | Case-specific NVS / Hair Rendering      | [91MB/model x 40]() | [benchmarks/instant-ngp](benchmarks/instant-ngp/README.md) | [400MB]()                |
| NeuS          | Case-specific NVS / Hair Rendering      | [OneDrive]() | [benchmarks/NeuS]() | [OneDrive]()                |
| MVP        | Case-specific NVS / Hair Rendering         | [OneDrive]() | [benchmarks/MVP]() | [OneDrive]()                |
| NV   | Case-specific NVS / Hair Rendering               | [OneDrive]() | [benchmarks/NV]() | [OneDrive]()                |
| IBRNet   | Generalizable NVS                            | [OneDrive]() | [benchmarks/IBRNet]() | [OneDrive]()                |
| KeypointNerf   | Generalizable NVS              | [OneDrive]() | [benchmarks/KeypointNerf]()       | [OneDrive]()                |
| VisionNerf   | Generalizable NVS                | [OneDrive]() | [benchmarks/VisionNerf]() |  [OneDrive]()  |
| NerFace   | Case-specific Novel Expression Synthesis              | [OneDrive]() | [benchmarks/NerFace]()       | [OneDrive]()                |
| IM Avatar   | Case-specific Novel Expression Synthesis              | [OneDrive]() | [benchmarks/IMavatar]()       | [OneDrive]()                |
| Point-Avatar   | Case-specific Novel Expression Synthesis              | [OneDrive]() | [benchmarks/point-avatar]()       | [OneDrive]()                |
| NSFF   | Hair Rendering              | [OneDrive]() | [benchmarks/NSFF]()       | [OneDrive]()                |
| NRNerf   | Hair Rendering              | [OneDrive]() | [benchmarks/NRNerf]()       | [OneDrive]()                |
| e4e   | Hair Editting              | [OneDrive]() | [benchmarks/e4e]()       | [OneDrive]()                |
| PTI   | Hair Editting              | [OneDrive]() | [benchmarks/PTI]()       | [OneDrive]()                |
| Restyle-e4e   | Hair Editting              | [OneDrive]() | [benchmarks/Restyle-e4e]()       | [OneDrive]()                |
| Hyperstyle   | Hair Editting              | [OneDrive]() | [benchmarks/Hyperstyle]()       | [OneDrive]()                |
| ADNerf   | Talking Head              | [OneDrive]() | [benchmarks/ADNerf]()       | [OneDrive]()                |
| SSPNerf   | Talking Head              | [OneDrive]() | [benchmarks/SSPNerf]()       | [OneDrive]()                |

## Usage
The code will be released in May

## TODO List

- [ ] Release Code and pretrained model
- [ ] Release Dataset
- [ ] Technical Report
- [x] Project page


## Related Works
## Citation

```bibtex
@article{2023renderme360,
      title={RenderMe-360: Large Digital Asset Library and Benchmark Towards High-fidelity Head Avatars"}, 
      author={},
      journal   = {arXiv preprint},
      volume    = {},
      year    = {2023}
```
## Acknowlegement
