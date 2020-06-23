# MonoclularDepth

This repository is for testing and comparing different approaches to monocular depth estimation.

## Requirements

Clone repository with submodules (`git clone --recurse-submodules ...`).

Install the submodules in editable mode
```bash
pip install -e monodepth2 
```

## Usage

### monodepth2

Use `infer_depth(model, img)` from `infer.py` to extract a depth array and a disparity image from and RGB image. The depth values will need to be scaled by a scalar value. For stereo-trained models on KITTI, this value is `5.4`.
