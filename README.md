# CycleGAN

Tensorflow implementation for learning an image-to-image translation **without** input-output pairs.
The method is proposed by [Jun-Yan Zhu](https://people.eecs.berkeley.edu/~junyanz/) in 
[Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/pdf/1703.10593.pdf). 

## Prerequisites
- tensorflow r1.1
- numpy 1.11.0
- scipy 0.17.0
- pillow 3.3.0

## Getting Started
### Installation
- Install tensorflow from https://github.com/tensorflow/tensorflow
- Clone this repo:
```bash
git clone https://github.com/jgriffi2/CS230-Project
cd CS230-Project
```

## Training and Test Details
To train a model,  
```bash
CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=/path/to/data/ 
```
Models are saved to `./checkpoints/` (can be changed by passing `--checkpoint_dir=your_dir`).  

To test the model,
```bash
CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=/path/to/data/ --phase=test --which_direction=AtoB/BtoA
```

## Reference
- Tensorflow implementation of CycleGAN, https://github.com/xhujoy/CycleGAN-tensorflow
