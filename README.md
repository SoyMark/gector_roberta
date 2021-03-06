# Grammatical Error Correction

This repository is slightly modified on the original code repository:

> https://github.com/MaksTarnavskyi/gector-large

which can nearly reach the performance of SOTA (2021) 

> [A Simple Recipe for Multilingual Grammatical Error Correction](https://arxiv.org/pdf/2106.03830.pdf)



## Installation
The following command installs all necessary packages:
```.bash
conda create -n GEC python=3.7
conda activate GEC
pip install -r requirements.txt
```
The project was tested using Python 3.7 on both Ubuntu 20.04 and Windows 10.

#### Model

download model from

> https://drive.google.com/file/d/1HujoTB_tcAaCkA5OZ9RRAAD9ZoPWpyr0/view?usp=sharing

then move this file into "./model"

## Usage

Enter the input text into "./input/input.txt", then:

```python
python predict.py
```

The output will be in "./output/output.txt"

The input text will be handled by the model line by line(128 lines per batch). the default `max_len` is 100, and the default `min_len` is 1. Make sure each line of input comes within that range!  You can modify those parameters in predict.py if you want.
