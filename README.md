## StyleGAN &mdash; Official TensorFlow Implementation
![Python 3.6](https://img.shields.io/badge/python-3.6-green.svg?style=plastic)
![TensorFlow 1.10](https://img.shields.io/badge/tensorflow-1.10-green.svg?style=plastic)
![cuDNN 7.3.1](https://img.shields.io/badge/cudnn-7.3.1-green.svg?style=plastic)
![License CC BY-NC](https://img.shields.io/badge/license-CC_BY--NC-green.svg?style=plastic)



Usage:
1. 搭建环境：
conda create -n stylegan python=3.6
pip install tensorflow-gpu==1.13.1,pillow,requests,scipy
512 * 512 GPU Memory 8779MiB

2. run:
python train.py


3. 将训练图片转换成tf-record，现在转换好的已经在datasets目录下
                                               转换后的路径                          原路径                                     
python dataset_tool.py create_from_images datasets/jellyfish /Users/xufeng/Data/Jellyfish/recognizer/true_filter_256
python dataset_tool.py create_from_images datasets/horse /Users/xufeng/Projects/AI-Painting-horse/horse
python dataset_tool.py create_from_images datasets/horse /home/data_user/xufeng/Code/NST/StyleGAN/datasets_ori/horse-V5



```

Training times for the default configuration using Tesla V100 GPUs:

| GPUs | 1024&times;1024  | 512&times;512    | 256&times;256    |
| :--- | :--------------  | :------------    | :------------    |
| 1    | 41 days 4 hours  | 24 days 21 hours | 14 days 22 hours |
| 2    | 21 days 22 hours | 13 days 7 hours  | 9 days 5 hours   |
| 4    | 11 days 8 hours  | 7 days 0 hours   | 4 days 21 hours  |
| 8    | 6 days 14 hours  | 4 days 10 hours  | 3 days 8 hours   |

