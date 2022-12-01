# MargNet
A repository containing our code for our paper, "Photometric identification of compact galaxies, stars and quasars using multiple neural networks".


# Paper Links:
[![Paper DOI](https://img.shields.io/badge/MNRAS-10.1093%2Fmnras%2Fstac3336-blueviolet)](https://doi.org/10.1093/mnras/stac3336)
[![arXiv](https://img.shields.io/badge/arXiv-astro--ph%2F2211.08388-red)](https://arxiv.org/abs/2211.08388) 
[![Dataset+Models](https://zenodo.org/badge/DOI/10.5281/zenodo.6659435.svg)](https://doi.org/10.5281/zenodo.6659435)

You can also access the MNRAS version using our [free-access link](https://academic.oup.com/mnras/advance-article/doi/10.1093/mnras/stac3336/6831636?utm_source=authortollfreelinkguestAccessKey=10ada097-d979-4037-84af-c72d47f5c21b).


# Abstract
We present MargNet, a deep learning-based classifier for identifying stars, quasars and compact galaxies using photometric parameters and images from the Sloan Digital Sky Survey (SDSS) Data Release 16 (DR16) catalogue. MargNet consists of a combination of Convolutional Neural Network (CNN) and Artificial Neural Network (ANN) architectures. Using a carefully curated dataset consisting of 240,000 compact objects and an additional 150,000 faint objects, the machine learns classification directly from the data, minimising the need for human intervention. MargNet is the first classifier focusing exclusively on compact galaxies and performs better than other methods to classify compact galaxies from stars and quasars, even at fainter magnitudes. This model and feature engineering in such deep learning architectures will provide greater success in identifying objects in the ongoing and upcoming surveys, such as Dark Energy Survey (DES) and images from the Vera C. Rubin Observatory.

# Directory Structure
Our code is organized as follows.

Experiment 1 - Contains the dataset and the jupyter notebooks used for experiment 1.
Experiment 2 - Contains the dataset and the jupyter notebooks used for experiment 2.
Experiment 3 - Contains the dataset and the jupyter notebooks used for experiment 3.

Not all files could be included on GitHub due to storage limit, so a complete copy of the repository has also been mirrored on Zenodo: (https://doi.org/10.5281/zenodo.6659435).

# A note on the dataset:
The datasets have been organized by each experiment, and this is what each file means:
* `objlist.npy` - The SDSS ObjID of each object
* `X.npy` - the 5-band image for each object (Used by the CNN)
* `dnnx.npy` - the set of 24 photometric features for each object (Used by the DNN)
* `y.npy` - the classification label for each object
* `photofeatures.csv` - SDSS spreadsheet containing all the features from dnnx, labels from y, ObjIDs from objlist and a couple of more SDSS specific parameters.

Note: objlist, X, dnnx and y are in the same order. So, `objlist[0]`, `X[0]`, `dnnx[0]` and `y[0]` correspond to the same object.

# Authors
Siddharth Chaini, Atharva Bagul, Anish Deshpande, Rishi Gondkar, Kaushal Sharma, M Vivek, Ajit Kembhavi
