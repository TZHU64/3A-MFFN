# 3D Atrous Spatial Pyramid Pooling based Multi-Scale Feature Fusion Network for Hyperspectral Image Classification

This code is the implements of ["3D Atrous Spatial Pyramid Pooling based Multi-Scale Feature Fusion Network for Hyperspectral Image Classification" in 2023 International Conference on Remote Sensing, Mapping and Geographic Information Systems (RSMG 2023)]

## Requirements

`pip install -r requirements.txt`

## Hyperspectral datasets

Several public hyperspectral datasets are available on the [UPV/EHU](http://www.ehu.eus/ccwintco/index.php?title=Hyperspectral_Remote_Sensing_Scenes) wiki. Users can download those beforehand. The default dataset folder is `./Datasets/`.

## Usage

Start a Visdom server:
`python -m visdom.server`
and go to [`http://localhost:8097`](http://localhost:8097) to see the visualizations (or [`http://localhost:9999`](http://localhost:9999) if you use Docker).

Then, run the script `main.py`

The most useful arguments are:

  * `--model` to specify the model (e.g. 'svm', 'nn', 'hamida', 'lee', 'chen', 'li'),
  * `--dataset` to specify which dataset to use (e.g. 'PaviaC', 'PaviaU', 'IndianPines', 'KSC', 'Botswana'),
  *  `--cuda` switch to run the neural nets on GPU. The tool fallbacks on CPU if this switch is not specified.

Example:

  * `python main.py --model ASPP --dataset IndianPines --training_sample 0.1 --cuda 0`

