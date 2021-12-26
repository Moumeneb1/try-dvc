This repo version controls ASR training data

# How to USE dvc (data version controlling)

First you need to install the dvc 


```bash
pip install dvc
```

To use this dataset in your project repo, add it as a submodule, in your project code 

```bash
git submodule add https://github.com/Moumeneb1/try-dvc
```

This will clone the gitlab data model, if you wanna track the specefic version of the dataset used on for the ressults, otherwise just use, git clone/ 


We use git tags to track versions of our dataset, 

use git checkout to switch to specific versions, of datasets

```bash
git checkout tags/v1.0
```

Now you need to add the remote dvc file 

```bash
dvc remote add -d storage gdrive://1c-tFhMoms1PhkN7J4NcS8OswpDJOGJds
```

Now your dvc points to the datastorage ( where the data is actually stored), you can now pull the dataset you need 
```bash
dvc pull dataset.dvc
```
