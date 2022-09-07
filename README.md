# Restoration-of-Degraded-Images-Using-VAE-and-GAN
This project is my final year project implementation and is all about restoring Degraded Images using VAE and GAN.

## Demo

[embed]C16_PPT.pdf[/embed]

![image](https://user-images.githubusercontent.com/48184601/184223352-e1368dae-fc9f-47d5-bfb9-7d654fa7b82d.png)


## Requirement
The code is tested on Ubuntu with Nvidia GPUs and CUDA installed. Python>=3.6 is required to run the code.

## Installation

Clone the Synchronized-BatchNorm-PyTorch repository for

```
cd Face_Enhancement/models/networks/
git clone https://github.com/vacancy/Synchronized-BatchNorm-PyTorch
cp -rf Synchronized-BatchNorm-PyTorch/sync_batchnorm .
cd ../../../
```

```
cd Global/detection_models
git clone https://github.com/vacancy/Synchronized-BatchNorm-PyTorch
cp -rf Synchronized-BatchNorm-PyTorch/sync_batchnorm .
cd ../../
```

Download the landmark detection pretrained model

```
cd Face_Detection/
wget http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
bzip2 -d shape_predictor_68_face_landmarks.dat.bz2
cd ../
```

Download the pretrained model from Azure Blob Storage, put the file `Face_Enhancement/checkpoints.zip` under `./Face_Enhancement`, and put the file `Global/checkpoints.zip` under `./Global`. Then unzip them respectively.

```
cd Face_Enhancement/
wget https://facevc.blob.core.windows.net/zhanbo/old_photo/pretrain/Face_Enhancement/checkpoints.zip
unzip checkpoints.zip
cd ../
cd Global/
wget https://facevc.blob.core.windows.net/zhanbo/old_photo/pretrain/Global/checkpoints.zip
unzip checkpoints.zip
cd ../
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## How to use?
**Note**: GPU can be set 0 or 0,1,2 or 0,2; use -1 for CPU
