# Creating the data files

You can obtain all the three datasets from [Google Drive](https://drive.google.com/drive/folders/1ZqaPd78kNRLBjmkWNEM8420NWllfmdkM?usp=sharing).

## The *Whale* dataset

The dataset was downloaded from [timeseriesclassification.com](http://www.timeseriesclassification.com/). Due to ongoing maintenance on the original website, all datasets from [timeseriesclassification.com](http://www.timeseriesclassification.com/) are temporarily available at [zenodo.org](https://www.zenodo.org). The dataset includes 10,934 instances for training and 1,962 instances for testing. Each instance is a two-second audio segment sampled at a rate of 2 kHz, resulting in a series length 4000. The dataset was subdivided into training, validation, and testing sets with proportions of 60%, 20%, and 20%, respectively.

Therefore, the following csv files were used with the audio filenames.
[Google Drive](https://drive.google.com/drive/folders/1ZqaPd78kNRLBjmkWNEM8420NWllfmdkM?usp=sharing).

### Example

To create the dataset files just run the 'load_data.ipynb' file. 
