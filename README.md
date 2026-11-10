# CoSMoNet

This project provides the code and results for 'CoSMoNet: Optical Remote Sensing Saliency Detection via Count-Adaptive Sparse Transfer and Moment-Guided Reconstruction'.

All code, results, and checkpoints are distributed in a single Baidu Netdisk archive (see [Download](#download)). The training / testing settings and the datasets are the same as those used in [GeleNet](https://github.com/MathLee/GeleNet), i.e., EORSSD and ORSI-4199.

# Download

All code, results (including saliency maps), and checkpoints of CoSMoNet are packed in `ttest.zip`:

- File: `ttest.zip`
- Link: https://pan.baidu.com/s/1aVWMcsAcWDCZXc6aoEoqZg?pwd=c6zc
- Extraction code (提取码): `c6zc`

Download and unzip the archive before following the instructions below. The released code keeps the original script names (e.g., `train_GeleNet.py`, `test_GeleNet.py`).

# Network Architecture

See the paper and the model definition in the released code archive for the network architecture of CoSMoNet.

# Requirements

python 3.8 + pytorch 1.9.0

# Saliency maps

We provide saliency maps of our CoSMoNet on two datasets in `ttest.zip` (PVT-v2-b2 backbone and Swin Transformer backbone).

# Training

Download [pvt_v2_b2.pth](https://pan.baidu.com/s/1U6Bsyhu0ynXckU6EnJM35w) (code: sxiq), and put it in './model/'.

Modify paths of datasets, then run train_GeleNet.py.

Note: Our main model is under './model/GeleNet_models.py' (PVT-v2-b2 backbone).

# Pre-trained model and testing

1. Download `ttest.zip` (see [Download](#download)) and put the pre-trained models (PVT-v2-b2 backbone) on EORSSD and ORSI-4199 in './models/'.
2. Modify paths of pre-trained models and datasets.
3. Run test_GeleNet.py.

# Evaluation Tool

You can use the [evaluation tool (MATLAB version)](https://github.com/MathLee/MatlabEvaluationTools) to evaluate the above saliency maps.

# Citation

If you use this code or the released results, please cite our paper:

```bibtex
@ARTICLE{CoSMoNet,
        title   = {CoSMoNet: Optical Remote Sensing Saliency Detection via Count-Adaptive Sparse Transfer and Moment-Guided Reconstruction},
        }
```

This repository follows the training / testing protocol and datasets of GeleNet (IEEE TIP 2023). Please also cite:

```bibtex
@ARTICLE{Li_2023_GeleNet,
        author  = {Gongyang Li and Zhen Bai and Zhi Liu and Xinpeng Zhang and Haibin Ling},
        title   = {Salient Object Detection in Optical Remote Sensing Images Driven by Transformer},
        journal = {IEEE Transactions on Image Processing},
        volume  = {32},
        pages   = {5257-5269},
        year    = {2023},
        }
```

If you encounter any problems with the code, want to report bugs, etc.

Please contact me at jhzhou22@mails.jlu.edu.cn.
