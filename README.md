# Skin Disease Classification
Favis et al.'s models for Skin Disease Classification
# Prerequisites
- download datasets & trained models from GDrive (~ 3-4gb)
- Python, PIP, Anaconda
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
- `pip install -U openmim`
- `mim install mmengine`
- `mim install "mmcv>=2.0.0"`
- `mim install mmdet`
## Updates to Code
```
# reduce imports -> no longer supported
from mmdet.apis import init_detector, inference_detector
# from mmcv import Config -> no longer supported
from mmengine.config import Config
```
## Guides
- [Installation issue w/ mmcv](https://github.com/open-mmlab/mmcv/issues/1055)
- [Import Issue w/ Config](https://stackoverflow.com/questions/75988459/cannot-import-name-config-from-mmcv-unknown-location)