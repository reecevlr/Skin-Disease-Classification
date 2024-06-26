# Skin Disease Classification
Favis et al.'s models for Skin Disease Classification
# Prerequisites
- download datasets & trained models from GDrive (~ 3-4gb)
- Python, PIP, Virtual Environment
# Installing dependencies
*Install **within** active environment*
- `pip install -r dependencies.md`
  - will install all dependencies welcome buddy boy
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
