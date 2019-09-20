# Deep Directional Statistics: Pose Estimation with Uncertainty Quantification.



* [Installation](#installation)
* [Datasets](#datasets)
    * [PASCAL3D+](#pascal3d)
* [Training](#training)
* [Pre-trained Models](#pre-trained-models)
* [Citing](#citing)
* [References](#refs)

## Installation  

```
bash scripts/install.sh
```

This will create a virtual environment for the project (located in 
"$PROJECT_DIR/py_env" folder) and install all necessary dependencies 
(TensorFlow, Keras, etc.).

To work with available notebooks, run:

```
bash scripts/start_notebook.sh
```

## Datasets

### PASCAL3D+

Download [the preprocessed data](https://drive.google.com/open?id=1baI_QUNuGN9DJGgaOWubbservgQ6Oc4x) and place it into 
"$PROJECT_DIR/data" folder.

Note: all angles are stored in biternion (cos, sin) representation. Converters to degrees\radians are available at 
utils/angles.py

See [demo notebook](https://github.com/sergeyprokudin/deep_direct_stat/blob/master/notebooks/PASCAL3D%2B%20Data%20Loading%20Demo.ipynb)
for an example of loading.

## Training

To train on one of PASCAL3D+ classes,run:

```
source py_env/bin/activate
python training_scripts/train_pascal3d.py CLS_NAME
``` 

where CLS_NAME is one of the PASCAL classes (aeroplane, car, ...)

Alternatively, see the [demo notebook](https://github.com/sergeyprokudin/deep_direct_stat/blob/master/notebooks/Pascal3D%2B%20training.ipynb)
for a step-by-step training procedure.

## Pre-trained Models

Download [pretrained models](https://drive.google.com/file/d/1H29OVZn5jdlQDQt6_R7eK7WOEinmgxcy/view?usp=sharing).

See [demo notebook](https://github.com/sergeyprokudin/deep_direct_stat/blob/master/notebooks/Pascal3D%2B%20Model%20Demo.ipynb)
for an example of loading, predicting and evaluating pre-trained PASCAL3d+ models.

## Citing

```
@conference{deepdirectstat2018,
  title = {Deep Directional Statistics: Pose Estimation with Uncertainty Quantification},
  author = {Prokudin, Sergey and Gehler, Peter and Nowozin, Sebastian},
  booktitle = {European Conference on Computer Vision (ECCV)},
  month = sep,
  year = {2018},
  month_numeric = {9}
}
```

ArXiv preprint:

 - https://arxiv.org/pdf/1805.03430.pdf

## References 

 - https://github.com/lucasb-eyer/BiternionNet (original BiternionNet repository)
 - https://github.com/ShapeNet/RenderForCNN (used for getting PASCAL3D+ dataset and evaluation)



