**1. Main Environments.** </br>
The environment installation procedure can be followed by [VM-UNet](https://github.com/JCruan519/VM-UNet), or by following the steps below:</br>
Python version should be greater than 3.8
```
pip install cupy_cuda12x==13.2.0
pip install einops==0.8.0
pip install h5py==3.11.0
pip install mamba_ssm==2.0.3
pip install matplotlib==3.9.2
pip install MedPy==0.5.1
pip install numpy==2.1.1
pip install Pillow==10.4.0
pip install scikit_learn==1.5.1
pip install scipy==1.14.1
pip install SimpleITK==2.3.1
pip install SimpleITK==2.4.0
pip install thop==0.1.1.post2209072238
pip install timm==0.4.12
pip install torch==2.3.0
pip install torchvision==0.18.0
pip install tqdm==4.66.4

```
Download the pre-trained weights file here [this](https://zenodo.org/records/13743856).Put the downloaded pre-trained files into the ./pre_trained_weights folder.
**2. Datasets.** </br>
Download dataset from [this](https://zenodo.org/records/13741332) link.
*A.ISIC2017* </br>
1. Dataset introduction click this link [this](https://challenge.isic-archive.com/data)</br>

*B.ISIC2018* </br>
1. Dataset introduction click this link [this](https://challenge.isic-archive.com/data)</br>

*C.Synapse* </br>
1. Dataset introduction click this link [this](https://www.synapse.org/#!Synapse:syn3193805/wiki)</br>

*D.ACDC* </br>
1. Dataset introduction click this link [this](https://acdc.vision.ee.ethz.ch/). </br>

**3. Train the Mc-Mamba.**
```
python train.py --datasets_name <dataset name> --epochs 500 --batch_size 24 --work_dir <output dir>
```
**4. Test the Mc-Mamba.**  
```
python test.py --datasets_name <dataset name> --epochs 500 --batch_size 24 --work_dir <output dir> --best_model_path <the best weight path>
```

## Acknowledgement
Thanks to [VMamba](https://github.com/MzeroMiko/VMamba), [VM-UNet](https://github.com/JCruan519/VM-UNet) and [UltraLight-VM-UNet](https://github.com/wurenkai/UltraLight-VM-UNet) for their outstanding work.
