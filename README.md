
# DSB2018 [ods.ai] topcoders 1st place solution 
### For Model & Mothod introduction, please check [here](https://github.com/selimsef/dsb2018_topcoders/).
### This fork is for environment seting.

## [Code that I've done some change.](https://drive.google.com/file/d/19DyuLzYWclJWs3E6azTAcYlCV8grubK9/view?usp=sharing)
### use
```
git log
```
To see the code changing history

## Overall

#### There are three people, Selim, Albu, and Victor work together in this solution.
#### We need to run their's code separately.
#### I suggest creating three different virtualenv for each one.

### The Overall environment is:
cuda 10.0(The latest version is cuda 10.1, so maybe you need to downgrade).

use 
```nvcc --version```
to check

## Selim's

```
pip install imgaug
pip install lightgbm
pip install tqdm
pip install tensorflow-gpu==2.0.0
pip install Keras==2.3.1
pip install Keras-Applications==1.0.8
pip install opencv-python==4.1.2.30
pip install keras-resnet

```
After that, run:
```
../selim/predict_test.sh
```
## Albu's
```
pip install imgaug
pip install lightgbm
pip install tqdm
pip install torch==0.3.1
pip install torchvision==0.2.1
pip install opencv-python==4.1.2.30
pip install scipy==1.1.0
pip install pandas
pip install tensorboardX
```
After that, run:
```
../albu/src/predict_test.sh
```

## Victor's
```
pip install imgaug
pip install lightgbm
pip install tqdm
pip install tensorflow-gpu==2.0.0
pip install Keras==2.3.1
pip install Keras-Applications==1.0.8
pip install opencv-python==3.4.2.16 
pip install pandas
pip install scikit-learn==0.19
```
After that, run:
```
../victor/predict_test.sh
```
## For create_submissions Fails
#### If the memory can't create a submission for all test data, you can split the files into two segments (about 1500 files). 
#### In folder merged_test (It should have 3019 files inside.) and in merged_extend_test (It should have 3019 files inside, too.)
#### It should be like:
```
- (predictions)
  - (merged_test1)
  - (merged_test2)
  - (merged_extend_test1)
  - (merged_extend_test2)
```
#### Then run ```python create_submissions.py``` for two times.
#### After that, merge the two csv files into one.
