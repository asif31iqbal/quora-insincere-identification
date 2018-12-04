# Quora insincere questions identification with Multi-ratio sampling, LSTM and Capsules

All the relevant code of the project is in the jupyter notebook file [quora_project.ipynb](https://github.com/asif31iqbal/quora-insincere-identification/blob/master/project_quora.ipynb). The file is self-contained, however, you do need to prepare the python environment and install required dependencies as described below. The file has 

## Setup
I have personally used the [Anaconda](https://www.anaconda.com) distribution for downloading all required packages and creating my virtual environment for this. You can use `pip` for your purposes. For a proper execution of my code, Python version `3.6.6` is needed. Ideally any version above `3.6.6` should also work, but since I am using `Keras` with `Tensorflow` backend and `Tensorflow` seems to have some issues with Python `3.7`, I have decided to stick to version `3.6.6`.

To mimic my setup steps, do the following:

### Setting up the environment and packages
- Install Python `3.6.6` from [here](https://www.python.org/downloads/release/python-366/)
- Install Anaconda by following the instructions [here](https://conda.io/docs/user-guide/install/index.html) 
- Create a conda virtual environment `conda create --name {your_env_name}`
- Activate the environment `conda activate {your_env_name}`
- Install following packages:
```
conda install numpy
conda install pandas
conda install scikit-learn
conda install matplotlib
conda install nltk
conda install seaborn
conda install -c conda-forge keras
conda install jupyter
```

### Download the data
- Clone this git repository
- `cd` to the directory of the repository
- Install Kaggle API `pip install kaggle --upgrade`
- Assuming you have a Kaggle account, follow the commnads [here](https://github.com/Kaggle/kaggle-api) regarding **API Credentials** so that you are able to invoke the kaggle API methods. 
  - Create a new Kaggle API Token from you Kaggle's profile page
  - Download the created `kaggle.json` file and copy to a directory called `.kaggle` under your home directory
  - `chmod 600 ~/.kaggle/kaggle.json`
- Create data directory `mkdir data`
- `cd data`
- Download the Kaggle competitions files by invoking `kaggle competitions download quora-insincere-questions-classification`
- For our purposes, we only need 3 files out of the downloaded files. Unzip the files and copy `train.csv`, `test.csv` and `glove.840B.300d.txt`. Copy these 3 files right under the `data` directory.

That's it!! You are all set. At this point just run `jupyter notebook`, open the `quora_project.ipynb` file and run step by step or whatever way you want.


