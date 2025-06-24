## Train Dataset
The evaluation dataset can be found [here](https://www.dropbox.com/t/2Amyu4D5TulaIofv).
And using in (1) `n01440764` - containing **real** images for RealYoutube
             (2) `n01443537` - containing **fake** images for FaceSwap

## Evaluation Dataset
The evaluation dataset can be found [here](https://www.dropbox.com/t/2Amyu4D5TulaIofv).
And using in (1) `n01440764` - containing **real** images for RealYoutube
             (2) `n01443537` - containing **fake** images for NeuralTextures

**Important!!** <br />
Download and extract **weights.zip** in the same folder as `evaluate.py`

# Installation Guide
This code is built on top of [Dassl.pytorch](https://github.com/KaiyangZhou/Dassl.pytorch), so you need to install the `dassl` environment first. `cd` to `dassl` folder and simply follow the instructions described below: 

```bash
# Clone this repo
git clone https://github.com/sohailahmedkhan/CLIPping-the-Deception.git
cd CLIPping-the-Deception/
cd dassl/

# Create a conda environment
conda create -y -n dassl python=3.8

# Activate the environment
conda activate dassl

# Install torch (requires version >= 1.8.1) and torchvision
# Please refer to https://pytorch.org/ if you need a different cuda version
conda install pytorch torchvision cudatoolkit=10.2 -c pytorch

# Install dependencies
pip install -r requirements.txt

# Install this library (no need to re-build if the source code is modified)
python setup.py develop

cd..

data/
└── progan_train/
    ├── classnames.txt
    ├── images/
    │   ├── train/
    │   │   ├── n01440764/
    │   │   │   ├── image1.jpg
    │   │   │   ├── image2.jpg
    │   │   │   └── ...
    │   │   ├── n01443537/
    │   │   │   ├── image1.jpg
    │   │   │   ├── image2.jpg
    │   │   │   └── ...
    │   ├── val/
    │   │   ├── n01440764/
    │   │   │   ├── image1.jpg
    │   │   │   ├── image2.jpg
    │   │   │   └── ...
    │   │   ├── n01443537/
    │   │   │   ├── image1.jpg
    │   │   │   ├── image2.jpg
    │   │   │   └── ...

`````

`n01440764` refers to **real** images, whereas, `n01443537` contains **fake** images.

# Result 
<img width="260" alt="Screenshot 2025-06-24 at 14 11 10" src="https://github.com/user-attachments/assets/1f8c3b7c-e54f-4d4e-bd01-5746b2aa1508" />

# Citations
If you use this code in your research, please kindly cite the following papers:
```
@inproceedings{khan2024clipping,
  title={CLIPping the Deception: Adapting Vision-Language Models for Universal Deepfake Detection},
  author={Khan, Sohail Ahmed and Dang-Nguyen, Duc-Tien},
  booktitle={Proceedings of the 2024 International Conference on Multimedia Retrieval},
  pages={1006--1015},
  year={2024}
}

@inproceedings{zhou2022cocoop,
    title={Conditional Prompt Learning for Vision-Language Models},
    author={Zhou, Kaiyang and Yang, Jingkang and Loy, Chen Change and Liu, Ziwei},
    booktitle={IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    year={2022}
}

@article{zhou2022coop,
    title={Learning to Prompt for Vision-Language Models},
    author={Zhou, Kaiyang and Yang, Jingkang and Loy, Chen Change and Liu, Ziwei},
    journal={International Journal of Computer Vision (IJCV)},
    year={2022}
}
```
