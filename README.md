
# Diff-UNet

Diff-UNet: A Diffusion Embedded Network for Volumetric Segmentation.

We design the Diff-UNet applying diffusion model to solve the 3D medical image segmentation problem.

Diff-UNet achieves more accuracy in multiple segmentation tasks compared with other 3D segmentation methods.

![](/imgs/framework.png)

## dataset 
The dataset is BraTS2020. You can find it and see the details in https://www.med.upenn.edu/cbica/brats2020/data.html

Once the data is downloaded, you can begin the training process. The data dir is:

```python
data_dir = "./datasets/brats2020/MICCAI_BraTS2020_TrainingData/"
```

## training 

Training use Pytoch DDP mode with four GPUs. You also can modify the parameters to use one GPU to train(refer to the train.py).

```bash
python train.py
```

## testing
When you have trained a model, please modify the model path, then run the code.
```bash
python test.py
```