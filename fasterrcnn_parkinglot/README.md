
The faster_rcnn_parking_training notebook trains a **PyTorch Faster R-CNN** model with **MobileNet V3 Large FPN** backbone to detect and classify parking spaces as **empty** or **occupied** using PyTorch.

**Tech Stack**: 
- torch (CUDA)
- torchvision

The PKLot dataset folder structure:

- `data/train`
- `data/valid`
- `data/test`
- one COCO annotation file per split: `_annotations.coco.json`

The notebook covers the following workflow:

- reading only the first `N` images and matching annotations from each split
- converting images and targets into tensors with `Dataset` and `DataLoader`
- saving checkpoints and loss history
- plotting and storing loss curves
- running inference on sample images and visualizing predictions

The dataset categories in this export are:

- `1 -> space-empty`
- `2 -> space-occupied`


The PKLot dataset contains 12,416 images of parking lots extracted from surveillance camera frames. There are images on sunny, cloudy, and rainy days and the parking spaces are labeled as occupied or empty. We have converted the original annotations to a variety of standard object detection formats by enclosing a bounding box around the original dataset's rotated rectangle annotations. For more information on the dataset visit: [Original PKLot Website](https://web.inf.ufpr.br/vri/databases/parking-lot-database/)

DATASET SOURCE INFORMATION
--------------------------
Dataset: PKLot (Parking Lot Dataset)

Original Authors: Almeida et al. (2015)

Distribution Source: Kaggle (downloaded from)
Download URL: [Kaggle PKLot Dataset](https://www.kaggle.com/datasets/ammarnassanalhajali/pklot-dataset)

**CITATION** :

```
@article{almeida2015pklot,
  title={PKLot--A robust dataset for parking lot classification},
  author={Almeida, Paulo and Oliveira, Luiz S and Silva Jr, Eunelson and Britto Jr, Alceu and Koerich, Alessandro},
  journal={Expert Systems with Applications},
  volume={42},
  number={11},
  pages={4937--4949},
  year={2015},
  publisher={Elsevier}
}
```



**ACKNOWLEDGMENT** (Distribution Source):
This dataset was accessed via Kaggle. I thank the Kaggle community and the 
original dataset uploader for making this dataset available through the platform.