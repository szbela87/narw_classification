# NARW classification
This is the code repository to the manuscript:

**Comparative analysis of deep neural networks for accurate
classification of North Atlantic Right Whale Calls: A case
study of single models and stacking methods**
 
## Project Description
The North Atlantic Right Whale (NARW) is a critically endangered species, necessitating effective
monitoring and conservation strategies. This study evaluates various convolutional neural network architectures for classifying NARW vocalizations, focusing on DenseNet-121, MobileNetV2, ResNet-9, and CFResNet-9 architectures. DenseNet-121 demonstrates superior performance with a test accuracy of 92.79% and a recall rate of 91.71%. In contrast, the Small CFResNet-9-16 model is highly efficient, achieving a test accuracy of 90.97%, while it is 62.3% smaller and requires 82.7% less training time. Furthermore, we employ simple stacking techniques on the two best-performing models, DenseNet-121 and Small CF-ResNet-9-16, using 5-fold cross-validation. This approach leverages the strengths of individual models, resulting in a stacked model that achieves a stateof-the-art test accuracy of 93.26% and a recall of 90.93%, surpassing all single model performances.
These findings significantly contribute to the development of robust methods for accurate
classification of NARW calls, thereby aiding in the monitoring and conserving of this endangered
species.

## Getting Started
### Environment Requirements

First, please make sure you have installed Conda. Then, the environment can be installed by:
```
conda create -n insect_classification python=3.8
conda activate insect_classification
pip install -r requirements.txt
```

### Data Preparation

You can obtain the dataset from [Google Drive](https://drive.google.com/drive/folders/1b2Jph_sFOuSLA0xMeiTpZgLIU1S1ixwZ?usp=sharing).

```
mkdir data
```
**Please put them in the `./data` directory.**



### Training Example
In the different directories, we provide the training and evaluation notebooks. 

For the single models, these directories are:
* `densenet_augm`
* `densenet_no_augm`
* `mobilenet_augm`
* `mobilenet_no_augm`
* `small_resnet-9_augm`
* `small_resnet-9_no_augm`
* `large_resnet-9_augm`
* `large_resnet-9_no_augm`
* `small_cf-resnet-9-16_augm`
* `small_cf-resnet-9-16_no_augm`
* `small_cf-resnet-9-64_augm`
* `small_cf-resnet-9-64_no_augm`
* `large_cf-resnet-9-16_augm`
* `large_cf-resnet-9-16_no_augm`

For the stacked models, these directories are:
* `densenet_augm_stacking`
* `densenet_no_augm_stacking`
* `small_cf-resnet-9-16_augm_stacking`
* `small_cf-resnet-9-16_no_augm_stacking`

Each training script produces 5 training sessions.

The output files, i.e. the best models and logs are in the `./whale_densenet121/results` directory after the training, these are:
* `best_model_{i}.pt` - the model with best validation accuracy from the i-th training,
* `inrun_results_{i}.csv` - the results during the training by the i-th training (just for logging),
* `train_results_{i}.csv` - the training results corresponding to the i-th training process,
* `valid_results_{i}.csv` - the validation results corresponding to the i-th training process.

Here, $i=0...4$.

To evaluate these results, and the `best_model_{i}`, $i=0...4$ models on the test set use the `*_eval.ipynb` notebooks in the corresponding directory.
 
## Best Models

The trained models are available at [Google Drive](https://drive.google.com/drive/folders/1OBI0CsXWovm1bjQyb7mOEhUxVMQ0oB1f?usp=sharing).

## About the dataset

The descriptions of how to generate the `.csv` files for the training and the testing set can be found in the `create_datasets` directory, i. e. [./create_datasets/Data_Readme.md](https://github.com/szbela87/narw_classification/blob/main/create_dataset/Data_README.md)
 
