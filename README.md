# Time Is MattEr: Temporal Self-supervision for Video Transformers (TIME)

PyTorch implementation for <a href=https://proceedings.mlr.press/v162/yun22a.html>"Time Is MattEr: Temporal Self-supervision for Video Transformers"</a> (accepted in ICML 2022)

<p align="center">
<img width="950" alt="thumbnail" src="https://user-images.githubusercontent.com/34064646/178366422-f7db1073-81ef-46c3-889d-eb55046ef7f6.png">
</p>

## Requirements
First, create a conda virtual environment and activate it:
```
conda create -n TIME python=3.7 -y
source activate TIME
```
Then, install the following packages:
```
"torch>=1.9.0"
"torchvision>=0.10.0",
"einops>=0.3",
"yacs>=0.1.6",
"pyyaml>=5.1",
"imageio",
"fvcore",
"timm",
"scikit-learn",
"av",
"matplotlib",
"termcolor>=1.1",
"simplejson",
"tqdm",
"psutil",
"matplotlib",
"scikit-build",
"cmake",
"opencv-python",
"pandas",
"sklearn",
'torchmeta',
"ffmpeg-python",
"tensorboard",
```


### Training codes
# TimeSformer 
```
python main.py --cfg configs/timesformer/ssv2/train.yaml
```

# Motionformer
```
python main.py --cfg configs/motionformer/ssv2/train.yaml
```

# X-ViT
```
python main.py --cfg configs/xvit/ssv2/train.yaml
```

## Acknowledgement
Our code base is built partly upon the packages: 
<a href="https://github.com/facebookresearch/SlowFast">SlowFast</a>, <a href=https://github.com/facebookresearch/TimeSformer>TimeSformer</a>, and <a href=https://github.com/rwightman/pytorch-image-models>pytorch-image-models</a> by <a href=https://github.com/rwightman>Ross Wightman</a>.

## Citation
If you use this code for your research, please cite our papers.
```
@InProceedings{pmlr-v162-yun22a,
  title = 	 {Time Is {M}att{E}r: Temporal Self-supervision for Video Transformers},
  author =       {Yun, Sukmin and Kim, Jaehyung and Han, Dongyoon and Song, Hwanjun and Ha, Jung-Woo and Shin, Jinwoo},
  booktitle = 	 {Proceedings of the 39th International Conference on Machine Learning},
  pages = 	 {25804--25816},
  year = 	 {2022},
  editor = 	 {Chaudhuri, Kamalika and Jegelka, Stefanie and Song, Le and Szepesvari, Csaba and Niu, Gang and Sabato, Sivan},
  volume = 	 {162},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {17--23 Jul},
  publisher =    {PMLR},
  pdf = 	 {https://proceedings.mlr.press/v162/yun22a/yun22a.pdf},
  url = 	 {https://proceedings.mlr.press/v162/yun22a.html},
  abstract = 	 {Understanding temporal dynamics of video is an essential aspect of learning better video representations. Recently, transformer-based architectural designs have been extensively explored for video tasks due to their capability to capture long-term dependency of input sequences. However, we found that these Video Transformers are still biased to learn spatial dynamics rather than temporal ones, and debiasing the spurious correlation is critical for their performance. Based on the observations, we design simple yet effective self-supervised tasks for video models to learn temporal dynamics better. Specifically, for debiasing the spatial bias, our method learns the temporal order of video frames as extra self-supervision and enforces the randomly shuffled frames to have low-confidence outputs. Also, our method learns the temporal flow direction of video tokens among consecutive frames for enhancing the correlation toward temporal dynamics. Under various video action recognition tasks, we demonstrate the effectiveness of our method and its compatibility with state-of-the-art Video Transformers.}
}
```
