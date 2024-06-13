# Skin Disease Classification
Favis et al.'s models for Skin Disease Classification
# Prerequisites
- download datasets & trained models from GDrive (~ 3-4gb)
- Python, PIP, Anaconda
- Clone `mmdet` from [github-mmdet-repo](https://github.com/open-mmlab/mmdetection)
- Create a parent folder containing both mmdet & this repo
# Resolving Errors (torch + mmcv + mmdet)
*Install **within** active environment*
- `conda create -n "openmmlab"`
- `conda activate openmmlab`
- `conda env list`
	- check applicable versions of Python
- `conda install python=3.x`
	- select closest version to *Python 3.7*
- `pip install pillow==9.0.1`
	- closest compatible version w/ other dependencies
- `pip install torch==2.0.0 -f https://download.pytorch.org/whl/cu117`
	- automatically updates to closest compatible version after installing other dependencies
	- version for devices with GPUs supported by CUDA
- `pip install -U openmim`
- `mim install mmengine`
- `mim install "mmcv>=2.0.0"`
- `mim install mmdet` \
*Install supported pytorch*
- `pip uninstall pytorch torchvision torchaudio` | `conda uninstall pytorch torchvision torchaudio`
  - specific versions used: `pip install torch==2.0.0 torchvision==0.15.0 torchaudio==2.0.0`
- `pip cache purge` | `conda clean --all`
- `pip install pyyaml`
  - dependency of mmcv and mmengine
## Updates to Code
```
# reduce imports -> no longer supported
from mmdet.apis import init_detector, inference_detector

# from mmcv import Config -> no longer supported
from mmengine.config import Config

# updated paths for RetinaNet from mmdet package

# update to CPU only
model = init_detector(cfg, modelPath, device='cpu')
```
## Guides
- [Installation issue w/ mmcv](https://github.com/open-mmlab/mmcv/issues/1055)
- [Import Issue w/ Config](https://stackoverflow.com/questions/75988459/cannot-import-name-config-from-mmcv-unknown-location)
- [Assertion Error](https://stackoverflow.com/questions/57814535/assertionerror-torch-not-compiled-with-cuda-enabled-in-spite-upgrading-to-cud)
- Conda venv does not support 3.7, use python specific venv
  - [venv guide](https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/)
- shoot me