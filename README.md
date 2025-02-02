
<p align="center">
  <img src="https://github.com/Deeplite/neutrino-examples/raw/master/deeplite-logo-color.png" />
</p>

# Deeplite Neutrino Examples

Public examples to use [Deeplite Neutrino™](https://docs.deeplite.ai/neutrino/index.html) engine for model architecture optimization. 

> **_NOTE:_**  Make sure you have obtained either a free community license or a commercial support license, [from here](https://docs.deeplite.ai/neutrino/license.html)

## Classification Models

```{.python}
    python src/hello_neutrino_classifier.py --arch resnet18 --dataset cifar100 --delta 1
```

The pretrained architecture `models` and the `datasets` are loaded from the [Deeplite Torch Zoo](https://github.com/Deeplite/deeplite-torch-zoo). The `delta` of 1% denotes the maximum affordable reduction in the accuracy of the model during optimization. Feel free to play around with different classification models and datasets, along with different `delta` values to get different optimized results. The `arch` and the `datasets` can be customized with any native PyTorch pretrained model.

## Object Detection Models

Different object detection use-cases and examples are provided to play around with. 

To optimize a `SSD-300` model on [`VOC 2007 dataset`](http://host.robots.ox.ac.uk/pascal/VOC/), run the following,

```{.python}
    python src/hello_neutrino_ssd300.py --arch ssd300_resnet18 --delta 0.05
```

To optimize a `SSD-300` model with `Mobilenet_v2` backend on [`COCO dataset`](https://cocodataset.org/#home), run the following,

```{.python}
    python src/hello_neutrino_mb2ssd.py --arch mb2_ssd --delta 0.05
```

To optimize a `YOLOv3` model on [`VOC 2007 dataset`](http://host.robots.ox.ac.uk/pascal/VOC/), run the following,

```{.python}
    python src/hello_neutrino_yolov3.py --arch yolo3 --delta 0.05
```

The `delta` of 0.05 denotes the maximum affordable reduction in the mAP (Mean Average Precision) of the model during optimization. Feel free to play around with different object detection models and datasets, along with different `delta` values to get different optimized results. The `arch` and the `datasets` can be customized with any native PyTorch pretrained model.

## Segmentation Models

To optimize a `U-Net` style model backend on [`VOC 2007 dataset`](http://host.robots.ox.ac.uk/pascal/VOC/), run the following,
```{.python}
    python src/hello_neutrino_unet.py --dataset voc --delta 0.02
```

The `delta` of 0.02 denotes the maximum affordable reduction in the mIOU (Mean Intersection over Union) of the model during optimization. Feel free to play around with different segmentation models and datasets, along with different `delta` values to get different optimized results. The `arch` and the `datasets` can be customized with any native PyTorch pretrained model.


