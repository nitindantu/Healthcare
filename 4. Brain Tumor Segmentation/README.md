# Fully automatic Brain tumor segmentation

### Brief overview

This repository provides source code for a deep convolutional neural network architecture designed for brain tumor segmentation with BraTS2017 dataset. 
The architecture is fully convolutional network (FCN) built upon the well-known U-net model and it makes use of residual units instead of plain units to speedup training and convergence.
The Brain tumor segmentation problem exhibits severe class imbalance where the healthy voxels comprise 98% of total voxels,0.18% belongs to necrosis ,1.1% to edema and non-enhanced and 0.38% to enhanced tumor. 
The issue is addressed by: 1) adopting a patch-based training approach; 2) using a custom loss function that accounts for the imbalance. 
During training, 2D patches of size 128x128 from the axial plane are randomly sampled. And by doing so it allows to dismiss patches from pixels with zero intensity and therefore it helps a bit to alleviate the problem.

The implementation is based on keras and tested on both Theano and Tensorflow backends.

Here are some results predicted by a model trained for 2 epochs :

*   **HGG cases** :

![HGG-Brats17_2013_7_1-111](https://github.com/nitindantu/Healthcare/assets/41870240/d1a37642-eefd-4a0d-9afe-ebacb522db54)
![HGG-Brats17_CBICA_ASV_1-88](https://github.com/nitindantu/Healthcare/assets/41870240/a34b88c5-3ac4-462f-8b59-311fc0e48451)
![HGG-Brats17_TCIA_186_1-90](https://github.com/nitindantu/Healthcare/assets/41870240/505fed33-29ef-40fe-a627-0537ed2d4f8c)

*   **LGG cases** :
![LGG-Brats17_TCIA_202_1-70](https://github.com/nitindantu/Healthcare/assets/41870240/00449b0b-c000-4b04-99d2-2fcbecab77da)
![LGG-Brats17_2013_24_1-91](https://github.com/nitindantu/Healthcare/assets/41870240/061b5896-2902-49c3-8e7e-8639e48fe9e1)
![LGG-Brats17_TCIA_462_1-97](https://github.com/nitindantu/Healthcare/assets/41870240/81f34321-5eb1-4bcf-b2fd-bc7347b587b9)


### Requirements

To run the code, you first need to install the following prerequisites: 

* Python 3.5 or above
* numpy
* keras
* scipy
* SimpleITK

### How to run

1. Execute first `extract_patches.py` to prepare the training and validation datasets.
2. then `train.py` to train the model.
3. `predict.py` to make final predictions.

```
python extract_patches.py
python train.py
python predict.py
```
