# MonocularDepth

This repository is for testing and comparing different approaches to monocular depth estimation.

## Requirements

Clone repository with submodules (`git clone --recurse-submodules ...`).

Install the submodules in editable mode
```bash
pip install -e monodepth2 mannequinchallenge
pip install torch torchvision scikit-image h5py
```

## Usage

### monodepth2

Use `infer_depth(model, img)` from `infer.py` to extract a depth array and a disparity image from an RGB image. The depth values will need to be scaled by a scalar value. For stereo-trained models on KITTI, this value is `5.4`.

### mannequinchallenge

Retrieve checkpoints by
```
cd mannequinchallenge
./fetch_checkpoints.sh
cd ..
```
Use `infer_depth(img)` from `infer.py` to extract a depth array and a disparity image from an RGB image. 
