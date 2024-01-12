# Introducing Language Guidance in Prompt Based Continual Learning 
![architecture](https://github.com/gulzainali98/LGCL/blob/main/LGCL.png)

This repository contains official PyTorch implementation code for Introducting Language Guidance in Prompt Based Continual Learning <a href="https://arxiv.org/pdf/2112.08654.pdf">LGCL</a>.



## Usage
First, clone the repository locally:
```
git clone https://github.com/gulzainali98/LGCL
cd LGCL
```
Then, install the packages below:
```
pytorch==1.12.1
torchvision==0.13.1
timm==0.6.7
pillow==9.2.0
matplotlib==3.5.3
```
Please use official CLIP repository for instructions on installing CLIP.

## Data preparation
If you already have CIFAR-100 or ImageNet-R, pass your dataset path to  `--data-path`.


The datasets aren't ready, change the download argument in `datasets.py` as follows

**CIFAR-100**
```
datasets.CIFAR100(download=True)
```

**ImageNet-R**
```
Imagenet_R(download=True)
```

## Training

Example Template

```
python main.py [config file] [args]
```

To train a model via command line on CIFAR-100 dataset:

```
python main.py cifar100_lgcl --model vit_base_patch16_224 --data-path /local-datasets/
```

## Evaluation
To evaluate a trained model:
```
python --use_env main.py <cifar100_lgcl or imr_lgcl> --eval
```


## License
This repository is released under the Apache 2.0 license as found in the [LICENSE](LICENSE) file.

## Cite

```
@inproceedings{khan2023introducing,
  title={Introducing language guidance in prompt-based continual learning},
  author={Khan, Muhammad Gul Zain Ali and Naeem, Muhammad Ferjad and Van Gool, Luc and Stricker, Didier and Tombari, Federico and Afzal, Muhammad Zeshan},
  booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision},
  pages={11463--11473},
  year={2023}
}
```


Thanks @JH-LEE-KR for providing the <a href="https://github.com/JH-LEE-KR/dualprompt-pytorch"> DualPrompt</a> pytorch code which was used in this repository. 
