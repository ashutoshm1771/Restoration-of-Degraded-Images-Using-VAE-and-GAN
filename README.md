# Restoration-of-Degraded-Images-Using-VAE-and-GAN
This project is my final year project implementation and is all about restoring Degraded Images using VAE and GAN.

## Demo

![image](https://user-images.githubusercontent.com/48184601/184223352-e1368dae-fc9f-47d5-bfb9-7d654fa7b82d.png)

##System Specs

![image](https://user-images.githubusercontent.com/48184601/188896033-105042c4-6444-4f72-8e9b-0b8d4b68e007.png)

![image](https://user-images.githubusercontent.com/48184601/188896107-db1e3795-d593-4a75-a96f-91afd346161c.png)

![image](https://user-images.githubusercontent.com/48184601/188896174-4fdc4289-4085-416a-bfd5-391239d7630b.png)

![image](https://user-images.githubusercontent.com/48184601/188950527-550f43a6-5f49-45f3-9ae5-76751c330e91.png)

![image](https://user-images.githubusercontent.com/48184601/188896229-22793488-3bcd-4a12-9eb1-3f0bf5497981.png)

![image](https://user-images.githubusercontent.com/48184601/188950648-0e230f80-db35-41c2-9992-50cda5174cf9.png)

![image](https://user-images.githubusercontent.com/48184601/188950689-f7e35154-e4ee-4ff6-a4f1-68ff899efde7.png)

![image](https://user-images.githubusercontent.com/48184601/188950729-8a2c1325-1e2d-4692-854e-521306f07ad5.png)

![image](https://user-images.githubusercontent.com/48184601/188950767-c7a232f9-453c-44ea-b4ad-246bf1afd3d7.png)

![image](https://user-images.githubusercontent.com/48184601/188950797-ff1819ae-54e5-4761-96f7-e589d2bec26e.png)

![image](https://user-images.githubusercontent.com/48184601/188950827-30f505c0-3ae7-46e2-b1e1-ea3759129d93.png)

![image](https://user-images.githubusercontent.com/48184601/188950857-4bab9de2-784f-4640-a77b-e47438388337.png)

![image](https://user-images.githubusercontent.com/48184601/188950938-1161cd2e-62c4-4f52-a751-07670f462b96.png)

![image](https://user-images.githubusercontent.com/48184601/188950972-f99bd5f2-6af8-437d-ac96-9d38107c3828.png)

![image](https://user-images.githubusercontent.com/48184601/188951020-3be930ae-0ceb-438e-8a86-9e466c7ae785.png)

![image](https://user-images.githubusercontent.com/48184601/188951059-71fdc480-e646-42b3-b871-6ec8b19a4960.png)

![image](https://user-images.githubusercontent.com/48184601/188951092-2b90af3c-5702-4a47-9296-2d9273acc1e2.png)

![image](https://user-images.githubusercontent.com/48184601/188951135-ff41b751-07ff-4702-84b8-f025bacd6b20.png)




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
