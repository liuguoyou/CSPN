# Depth Estimation via Affinity Learned with Convolutional Spatial Propagation Network

By Xinjing Cheng, Peng Wang and Ruigang Yang

## Contents
0. [Introduction](#introduction)
0. [Requirements](#requirements)
0. [Quick Guide](#quick-guide)
0. [Models](#models)
0. [Results](#results)
0. [Citation](#citation)

## Introduction

This repo contains the CNN models trained for depth completion from a RGB and sparse depth points, as described in the paper "[Depth Estimation via Affinity Learned with Convolutional Spatial Propagation Network](http://openaccess.thecvf.com/content_ECCV_2018/papers/Xinjing_Cheng_Depth_Estimation_via_ECCV_2018_paper.pdf)". The provided models are those that were used to obtain the results reported in the paper on the benchmark datasets NYU Depth v2 and KITTI for indoor and outdoor scenes respectively. Moreover, the provided code can be used for inference on arbitrary images. 

## Requirements

This code was tested with Python 3 and PyTorch 0.4.0.
- Install [PyTorch](http://pytorch.org/) on a machine with CUDA GPU.
- Install the [HDF5](https://en.wikipedia.org/wiki/Hierarchical_Data_Format) and other dependencies (files in our pre-processed datasets are in HDF5 formats).
	```bash
	sudo apt-get update
	sudo apt-get install -y libhdf5-serial-dev hdf5-tools
	pip3 install h5py matplotlib imageio scikit-image opencv-python
	```
- Download the preprocessed [NYU Depth V2](http://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html) and/or [KITTI Odometry](http://www.cvlibs.net/datasets/kitti/eval_odometry.php) dataset in HDF5 formats, and place them under the `data` folder. The downloading process might take an hour or so. The NYU dataset requires 32G of storage space, and KITTI requires 81G.
	```bash
	mkdir data; cd data
	wget http://datasets.lids.mit.edu/sparse-to-dense/data/nyudepthv2.tar.gz
	tar -xvf nyudepthv2.tar.gz && rm -f nyudepthv2.tar.gz
	wget http://datasets.lids.mit.edu/sparse-to-dense/data/kitti.tar.gz
 	tar -xvf kitti.tar.gz && rm -f kitti.tar.gz
	cd ..
	```

## Models

The trained models, namely **+UNet+CSPN** in the paper can be downloaded here:
- NYU Depth V2: 
- KITTI:

## Results

## Citation

If you use this method in your research, please cite: