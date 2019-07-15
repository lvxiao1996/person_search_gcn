# Person Search GCN Project
This project implements Context Graph of paper [Learning Context Graph for Person Search](https://arxiv.org/abs/1904.01830) (CVPR 2019 Oral). We are updating and will release more detailed code soon.

This repository shows how we can use graph convolution model to employ context information and improve person search performance. 

## Environment:
python(3.6),
pytorch(0.4.1),
numpy(1.14.1), 
matplotlib(3.0.2),
tqdm,
pickle


## Preparation

1. Clone this repo 

  ```Shell
  git clone https://github.com/sjtuzq/person_search_gcn.git
  ```

2. modify data_path, log_path and neighbor_num in config.py

3. download dataset [here](https://drive.google.com/open?id=1-pjZd-bZFTqV2F_34jr0q77-iEmjE4P5),then put it into data_path folder. This dataset features are generated by the method(slightly modified) in the paper [Joint Detection and Identification Feature Learning for Person Search](https://arxiv.org/abs/1604.01850), and the code can be found [here](https://github.com/ShuangLI59/person\_search). You can also utilize your own features.

4. prepare dataset 
  generate the raw data feature into the paired form: persons in the same images are grouped together.

  ```Shell
  python prepare.py
  ```

## Experiments

1. train and test the gcn model

  train graph convolution model: with the pair selected by distance.

  ```Shell
  python train_gcn1.py
  ```
  An example output:

  ```Shell
  epoch:0  acc:0.8269   map:0.8323
  ```
