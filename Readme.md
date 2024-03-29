Can We Evaluate Domain Adaptation Models Without Target-Domain Labels?
============================================================================

## Requirements
```
pytorch>=1.8.0
torchvision>=0.8.2
Python 3.8+
timm
```
## Dataset

Following datasets can be downloaded automatically into data folder:

- [Office31](https://www.cc.gatech.edu/~judy/domainadapt/)
- [OfficeHome](https://www.hemanthdv.org/officeHomeDataset.html)
- [VisDA2017](http://ai.bu.edu/visda-2017/)
- [DomainNet](http://ai.bu.edu/M3SDA/)

## Demo

To train a DAN method on Office31 D2A and save the model:
```
CUDA_VISIBLE_DEVICES=0 python dan.py data/office31 -d Office31 -s D -t A -a resnet50 --epochs 20 --seed 0 --log logs/dan/Office31_D2A
```
To calculate a DAN method's transfer score on Office31 D2A:
```
CUDA_VISIBLE_DEVICES=0 python dan.py data/office31 -d Office31 -s D -t A -a resnet50 --epochs 20 --seed 0 --log logs/dan/Office31_D2A --phase evaluation
```