# COCO instance segmentation

## Inference

Pretrained model can be dowloaded [here](https://drive.google.com/open?id=0B5DV6gwLHtyJZTR0NFllNGlwS3M).

```bash
# Pretrained model will be downloaded automatically
# or run below.
# python download_models.py

python demo.py
```

## Training

```bash
# Download datasets manually in ~/data/datasets/coco
# or run below.
# python download_datasets.py --all

python train.py --gpu 0
```

## Evaluation

### Inference

```bash
# Download datasets manually in ~/data/datasets/coco
# or run below.
# python download_datasets.py --val

python evaluate.py --data-dir /your/coco/dataset/dir
```

**FCIS ResNet101**

| Implementation | mAP/iou@[0.5:0.95] | mAP/iou@0.5 | mAP/iou@[0.5:0.95] \(small) | mAP/iou@[0.5:0.95] \(medium) | mAP/iou@[0.5:0.95] \(large) |
|:--------------:|:------------------:|:-----------:|:---------------------------:|:---------------------------:|:--------------------------:|
| [Original](https://github.com/msracver/FCIS) | 0.292 | 0.495 | 0.071 | 0.313 | 0.500|
| Ours | 0.259 | 0.444 | 0.058 | 0.271 | 0.466 |


## Dataset Download

- [COCO](http://cocodataset.org/)

```bash
# Dataset will be downloaded to ~/data/datasets/coco
python download_datasets.py --all
```
