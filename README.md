# PosDiffNet

Code for the paper:  
**"PosDiffNet: Positional Neural Diffusion for Point Cloud Registration in a Large Field of View with Perturbations"**

---

## 🛠 Requirements

### 1️⃣ PyTorch

The project is tested with **PyTorch 1.11.0 (CUDA 11.3)**.  
PyTorch 2.0 is also compatible.

#### Option A: Install via `pip`

```bash
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 \
--extra-index-url https://download.pytorch.org/whl/cu113
```

#### Option B: Install via `conda`

```bash
conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cudatoolkit=11.3 -c pytorch
```

---

### 2️⃣ Other Dependencies

```text
absl-py==0.12.0
cachetools==4.2.2
calmsize==0.1.3
google-auth==1.31.0
google-auth-oauthlib==0.4.4
grpcio==1.38.0
markdown==3.3.4
memory-profiler==0.58.0
oauthlib==3.1.1
opacus==0.15.0
opencv-python==4.5.5.64
pandas==1.2.4
protobuf==3.17.3
psutil==5.8.0
pyasn1==0.4.8
pyasn1-modules==0.2.8
pytorch-memlab==0.2.3
pytz==2021.1
requests-oauthlib==1.3.0
rsa==4.7.2
seaborn==0.11.2
tensorboard==2.5.0
tensorboard-data-server==0.6.1
tensorboard-plugin-wit==1.8.0
torch==1.8.0
torch-tb-profiler==0.1.0
torchvision==0.9.0
ttach==0.0.3
urllib3==1.26.5
werkzeug==2.0.1
```

Alternatively, you can directly create the conda environment:

```bash
conda env create -f env_code.yaml
```

---

## 📦 Dataset Preparation

Please prepare the following datasets:

- Fashion-MNIST  
- CIFAR-10  
- CIFAR-100  
- Tiny-ImageNet  

Make sure the dataset paths are configured properly before running the code.

---

## 🚀 Running the Code

```bash
screen -S f1
conda activate fl
cd ./system
python main.py -data Cifar10 -m cnn -algo FedNODE -nb 10 -gr 2000 -did 0
```

---

## 🔎 Code References

This implementation builds upon and benefits from the following open-source projects:

- https://github.com/rtqichen/torchdiffeq  
- https://github.com/huggingface/transformers  
- https://github.com/lxcnju/FedRepo  
- https://github.com/TsingZ0/FedALA  
- https://github.com/AvivSham/pFedHN  
- https://github.com/yuetan031/FedProto  
- https://github.com/TsingZ0/PFLlib  
