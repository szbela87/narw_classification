# NARW classification
 
## Project Description
The current study focuses on a comparative analysis of various deep learning architectures, namely MobileNetV2, DenseNet-121, ResNet-9, and CF-ResNet-9. The primary objective is to evaluate the performance of these models in classifying whale vocalizations in underwater audio recordings.

## Getting Started
### Environment Requirements

First, please make sure you have installed Conda. Then, our environment can be installed by:
```
conda create -n insect_classification python=3.8
conda activate insect_classification
pip install -r requirements.txt
```

**Important note:**
If you have and older GPU, i.e., a TESLA P4 then install an older PyTorch version:
```
pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113
```

### Data Preparation

You can obtain all the three datasets from [Google Drive](https://drive.google.com/drive/folders/1ZqaPd78kNRLBjmkWNEM8420NWllfmdkM?usp=sharing).

```
mkdir data
```
**Please put them in the `./data` directory.**



### Training Example
In the different directories, we provide the training scripts, i.e. for the *Whale* dataset and the large *ResNet9* model can be found
at `./whale_densenet121`. These directories are:
* `whale_densenet121`
* `whale_large-16_cf-resnet9`
* `whale_large_resnet9`
* `whale_mobilenetv2`
* `whale_small-16_cf-resnet9`
* `whale_small-64_cf-resnet9`
* `whale_small_resnet9`

The `small`/`large` words in the folder names indicate that the small/large *cf-resnet9* models were used on the corresponding dataset.

Each training script produces 5 training sessions.



The output files, i.e. the best models and logs are in the `./whale_densenet121/results` directory after the training, these are:
* `best_model_{i}.pt` - the model with best validation accuracy from the i-th training,
* `inrun_results_{i}.csv` - the results during the training by the i-th training (just for logging),
* `train_results_{i}.csv` - the training results corresponding to the i-th training process,
* `valid_results_{i}.csv` - the validation results corresponding to the i-th training process.

Here, $i=0...4$.

To evaluate these results, and evaluate the `best_model_{i}`, $i=0...4$ models on the test set use the following command:
 
It requires the files
`best_model_{i}.pt`, `inrun_results_{i}.csv`, `train_results_{i}.csv`, `valid_results_{i}.csv` for $i=0...4$ from the `results` available at [Google Drive](https://drive.google.com/drive/folders/1AVMsFHhytCohFgKaHfgesluDrLhLfnTa?usp=sharing), the file which contains evaluation metrics achieved by the model with the highest validation accuracy. 
 

## Best Models

The trained models are available at [Google Drive](https://drive.google.com/drive/folders/1AVMsFHhytCohFgKaHfgesluDrLhLfnTa?usp=sharing).
Further results are available at [Results.md](https://github.com/alargum/whale_vocalization_classification/blob/main/Results.md).

## About the datasets

The descriptions of how to generate the data files for the trainings and the tests can be found in the `create_datasets` directory, i. e. [./create_datasets/Data_Readme.md](https://github.com/alargum/whale_vocalization_classification/blob/main/create_dataset/Data_README.md)
 
