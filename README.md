chainer-fcis - FCIS
===================
![Build Status](https://travis-ci.org/knorth55/chainer-fcis.svg?branch=master)

![Example](static/example.png)

This is [Chainer](https://github.com/chainer/chainer) implementation of [Fully Convolutional Instance-aware Semantic Segmentation](https://arxiv.org/abs/1611.07709).

Original Mxnet repository is [msracver/FCIS](https://github.com/msracver/FCIS).

Requirement
-----------

- [CuPy](https://github.com/cupy/cupy)
- [Chainer](https://github.com/chainer/chainer)
- [ChainerCV](https://github.com/chainer/chainercv)
- OpenCV2

Additional Requirement
----------------------
- For COCO Dataset class
  - Cython
  - [pycocotools](https://github.com/cocodataset/cocoapi)

Notification
------------
- Only GPU implementation, No CPU implementation yet.
- Large GPU memory around 10GB is required (I use Titan X).

Installation
------------

```bash
# Requirement installation
# I recommend to use anacoda.

conda create -n fcis python=2.7
conda install -c menpo opencv
pip install cupy

# Installation

git clone https://github.com/knorth55/chainer-fcis.git
cd chainer-fcis
pip install -e .
```

Inference
---------

Pretrained models can be dowloaded [here](https://drive.google.com/open?id=0B5DV6gwLHtyJZTR0NFllNGlwS3M).

Inference can be done as below;

```bash
cd examples/coco/

python demo.py
```

Above is our implementation output, and below is original.

<img src="static/output.png" width="60%" >
<img src="static/original_output.png" width="60%" >

Training
--------

```bash
cd examples/coco/

python train.py --gpu 0
```

LICENSE
-------
[MIT LICENSE](LICENSE)


Powered by [DL HACKS](http://deeplearning.jp/hacks/)
