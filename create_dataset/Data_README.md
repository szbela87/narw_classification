# The *RightWhaleCalls* dataset

The origional form of the dataset is available at [timeseriesclassification.com](https://www.timeseriesclassification.com/description.php?Dataset=RightWhaleCalls). 

We created a new training/validation/test split using the entire dataset, with a ratio of 60/20/20%.
You can obtain the generated `.csv` files for the training and the test sets from [Google Drive](https://drive.google.com/drive/folders/1b2Jph_sFOuSLA0xMeiTpZgLIU1S1ixwZ?usp=sharing).

## Creating the `.csv` files for the numerical experiments

The dataset includes 10,934 instances for training and 1,962 instances for testing. Each instance is a two-second audio segment sampled at a rate of 2 kHz, resulting in a series length 4000.

To create the `.csv` files according to the 60/20/20% training/validation/test splitting, just run the `load_data.ipynb` notebook. 

