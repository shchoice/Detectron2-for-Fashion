# Fashion Image Instance segmentation with Detectron2

Facebook Ai Research(FAIR)에서 만든 Detectron2를 활용해 의류 이미지를 Instance Segmentation을 수행하였습니다.

![image-20200624021224570](https://user-images.githubusercontent.com/60699771/85435324-3d014e00-b5c2-11ea-8fa0-1475abd564e2.png)

![image-20200624021338235](https://user-images.githubusercontent.com/60699771/85435319-3b378a80-b5c2-11ea-98f0-2eaf08dd1cb3.png)



## Requirement

- Linux or macOS with Python ≥ 3.6
- Detectron2
- PyTorch ≥ 1.4
- torchivision that matches the PyTorch installation. You can install them together at [pytorch.org](https://pytorch.org) to make sure of this
- CUDA ≥ 10.1
- OpenCV, PIL to save RGBA type image
- pycocotools
- gcc &g++  ≥5 are required.



## Hardware

The model are trained using following hardware:

- Nvidia Tesla P4
- 32GB RAM



##  Datasets

Deep Fashion2 Dataset 활용(https://github.com/switchablenorms/DeepFashion2)

* training set : 19k

* validation set : 3.4k

* test set: 6k

* classes : 13 개
  

  ![image-20200624022140141](https://user-images.githubusercontent.com/60699771/85435321-3d014e00-b5c2-11ea-92c3-607707ee4514.png)
  
  

## Installation

```
pip install -U torch==1.5 torchvision==0.6 -f 
pip install -U 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
```



## Model

Model.zoo 에  있는 ResNEXT Pretrained 모델을 사용하여, 학습을 수행하였습니다.
