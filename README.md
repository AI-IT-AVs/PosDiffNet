# PosDiffNet

Code for the paper:  
**"PosDiffNet: Positional Neural Diffusion for Point Cloud Registration in a Large Field of View with Perturbations"**

This repository provides the **PyTorch implementation** of the PosDiffNet framework for large field-of-view point cloud registration.

## Datasets

We train and evaluate PosDiffNet on the following public datasets:

- **Boreas Dataset**  
  https://www.boreas.utias.utoronto.ca/

- **KITTI Dataset**  
  http://www.cvlibs.net/datasets/kitti/

Please download and prepare the datasets according to the official instructions before training or testing.

---

## Installation

Install the required packages and build the extensions using:

```bash
python setup.py build develop
```

The code has been tested under the following environment:
- Ubuntu 20.04  
- GCC 9.3.0  
- Python 3.8  
- PyTorch 1.7.1  
- CUDA 11.1  
- cuDNN 8.1.0  

---

## Training

Training and evaluation scripts are located in the `experiments/` directory.

To start training:

```bash
CUDA_VISIBLE_DEVICES=0 python train.py
```

---

## Testing

To evaluate a trained model:

```bash
CUDA_VISIBLE_DEVICES=0 python test.py --snapshot=../....pth.tar
```

Replace `../path_to_checkpoint.pth.tar` with the path to your trained model checkpoint.

---

## Acknowledgements

Our implementation builds upon several excellent open-source projects:

- https://github.com/twitter-research/graph-neural-pde  
- https://github.com/rtqichen/torchdiffeq  
- https://github.com/qinzheng93/GeoTransformer  
- https://github.com/magicleap/SuperGluePretrainedNetwork  
- https://github.com/huggingface/transformers  
- https://github.com/qiaozhijian/VCR-Net  
- https://github.com/iMoonLab/HGNN  
- https://github.com/Strawberry-Eat-Mango/PCT_Pytorch  
- https://github.com/WangYueFt/dcp  
