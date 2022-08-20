# Not Just Streaks: Towards Ground Truth for Single Image Deraining (ECCV'22)
Yunhao Ba<sup>1*</sup>, Howard Zhang<sup>1*</sup>, Ethan Yang<sup>1</sup>, Akira Suzuki<sup>1</sup>, Arnold Pfahnl<sup>1</sup>, Chethan Chinder Chandrappa<sup>1</sup>, Celso de Melo<sup>2</sup>, Suya You<sup>2</sup>, Stefano Soatto<sup>1</sup>, Alex Wong<sup>3</sup> Achuta Kadambi<sup>1</sup>

University of California, Los Angeles<sup>1</sup>, US Army Research Laboratory<sup>2</sup>, Yale University<sup>3</sup>

## Project Webpage
[https://visual.ee.ucla.edu/gt_rain.htm/](https://visual.ee.ucla.edu/gt_rain.htm/)

## Abstract
We propose a large-scale dataset of real-world rainy and clean image pairs and a method to remove degradations, induced by rain streaks and rain accumulation, from the image. As there exists no real-world dataset for deraining, current state-of-the-art methods rely on synthetic data and thus are limited by the sim2real domain gap; more- over, rigorous evaluation remains a challenge due to the absence of a real paired dataset. We fill this gap by collecting the first real paired deraining dataset through meticulous control of non-rain variations. Our dataset enables paired training and quantitative evaluation for diverse real-world rain phenomena (e.g. rain streaks and rain accumulation). To learn a representation invariant to rain phenomena, we propose a deep neural network that reconstructs the underlying scene by minimizing a rain- invariant loss between rainy and clean images. Extensive experiments demonstrate that our model outperforms the state-of-the-art deraining methods on real rainy images under various conditions.

## Citation

```
@InProceedings{ba2022gt-rain,
      author={Ba, Yunhao and Zhang, Howard, and Yang, Ethan and Suzuki, Akira and Pfahnl, Arnold and Chandrappa, Chethan Chinder and de Melo, Celso and You, Suya and Soatto, Stefano and Wong, Alex and Kadambi, Achuta},
      title={Not Just Streaks: Towards Ground Truth for Single Image Deraining},
      booktitle={ECCV},
      year={2022}
}
```

## Dataset
The dataset can be found [here](https://drive.google.com/drive/folders/1NSRl954QPcGIgoyJa_VjQwh_gEaHWPb8?usp=sharing).

## Requirements
All code was tested on Google Colab with the following:

- Ubuntu 18.04.6
- CUDA 11.2
- Python 3.7.13
- OpenCV-Python 4.6.0
- PyTorch 1.12.1
- scikit-image 0.18.3
- piq 0.7.0
## Setup
Download the dataset from the link above and change the parameters in the training and testing code to point to the appropriate directories.  

## Running
**Training:** After setting up the directory structure as specified above, simply run the training loop at the bottom of ```training_deraining_code.ipynb```. Additionally, model weights can be loaded from previous checkpoints by changing ```resume_train``` and ```model_path``` in the parameters section.

**Testing:** For testing, we provide two separate versions in ```testing_deraining_code.ipynb```, one for a generic test set which is done by specifying separate folders for the input rainy images and corresponding ground truths in the parameter section, and another for using our test set which can be downloaded from the the dataset link above. Our final model weights are located at ```model/model_checkpoint.pth```.

## Disclaimer
Please only use the code and dataset for research purposes.

## Contact
Yunhao Ba</br>
UCLA, Electrical and Computer Engineering Department</br>
yhba@ucla.edu

Howard Zhang</br>
UCLA, Electrical and Computer Engineering Department</br>
hwdz15508@g.ucla.edu
