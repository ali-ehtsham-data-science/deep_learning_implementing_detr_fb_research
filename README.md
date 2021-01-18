## Deep Learning Project for Implementing DETR
## Instructor: Satwat Bashir
## Group Member: Ammara Ihsan & Ali Ehtsham
## OS: Kali linux
## Python 3 

# Training DETR on Custom Dataset


In order to run this dataset please follow the instructions below

## Step 1.
Download wider face dataset [link](http://shuoyang1213.me/WIDERFACE/) and unzip the files in dataset folder

## Step 2.
Move to the dataset folder, and convert downloaded wider face dataset into COCO format
```
$ python face_to_coco.py
```

## Step 3.
Move to detr folder and run main.py
```
$ python -m torch.distributed.launch --nproc_per_node=[num_of_gpus] --use_env main.py --data_path ../dataset/
```

## Step 4.
Run test.py
```
$ python test.py --data_path ../dataset/WIDER_test/images/ --resume [path_to_checkpoint.pth]
```

## Thank you
## AE
