# Pusnet

This repo is the official code for

* [**Purified and Unified Steganographic Network**](https://openaccess.thecvf.com/content/CVPR2024/html/Li_Purified_and_Unified_Steganographic_Network_CVPR_2024_paper.html)
    
## Dependencies and Installation
- Python 3.8.13, PyTorch = 1.11.0
- Run the following commands in your terminal:

  `conda env create -f env.yml`

  `conda activate pyt_env`

## Get Started
#### Training
1. Change the code in `config.py`

    `line4:  mode = 'train' `

    `line14:  train_data_dir=''
   
    `line15:  test_data_dir=''
   
2. Run `python pusnet.py`

- Trained models will be saved in 'model_zoo' folder.

#### Testing
1. Change the code in `config.py`

    `line4:  mode = 'test' `
  
    `line36-41:  test_pusnet_path = '' `

2. Run `python pusnet.py`
  
- Testing results will be saved in 'results' folder.
- Here, we provide [trained models](https://drive.google.com/drive/folders/1lM9ED7uzWYeznXSWKg4mgf7Xc7wjjm8Q?usp=sharing).

## Dataset
- We train the PUSNet on the [DIV2K](https://opendatalab.com/DIV2K) training dataset, and test it on three [testing datasets](https://drive.google.com/file/d/1NYVWZXe0AjxdI5vuI2gF6_2hwoS1c4y7/view?usp=sharing), including the DIV2K test dataset, 1000 images randomly selected from the ImageNet test dataset
 
## Others
- The `batch_size` in `config.py` should be at least `2*number of gpus` and it should be divisible by number of gpus.


## Citation
If you find our paper or code useful for your research, please cite:
```
@inproceedings{li2024purified,
  title={Purified and Unified Steganographic Network},
  author={Li, Guobiao and Li, Sheng and Luo, Zicong and Qian, Zhenxing and Zhang, Xinpeng},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={27569--27578},
  year={2024}
}
```
