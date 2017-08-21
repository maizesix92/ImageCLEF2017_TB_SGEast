# Models for ImageCLEF2017: Tuberculosis task (SGEast)
This repository contains the weights of the neural network structures that we used in the ImageCLEF tuberculosis task. The team would like to share our models for further improvements.


### About the Task
The tuberculosis task can be further divided into 2 sub-tasks:
1) Multi-Drug-Resistant Detection (MDR)
2) Detection of Tuberculosis type (TBT)

More information about the challenge can be found on this website:
http://www.imageclef.org/2017/tuberculosis

### Libraries Used
We used 2 libraries for training our neural network. 
1. Caffe -- https://github.com/BVLC/caffe
2. Keras (with Theano backend) -- https://keras.io/ & http://deeplearning.net/software/theano/


### Performance
Below shows the performance of our models, based on the evaluation standards of the ImageCLEF committee. 
#### Task 1 (MDR Detection)
CNN-LSTM model

|          | AUC    | ACC    | Rank |
|----------|--------|--------|------|
| CNN-LSTM | 0.5620 | 0.5493 | 4    |

Rank 4 out of 28
#### Task 2 (TB-Type Detection)
CNN model

|                     | Kappa  | ACC    | Rank |
|---------------------|--------|--------|------|
| MAX pooling  policy | 0.2438 | 0.4033 | 1    |

Rank 1 out of 23
### Citations

If you have used our models, please cite this paper:

```
@inproceedings{sun11imageclef,
  title={ImageCLEF 2017: ImageCLEF tuberculosis task-the SGEast submission},
  author={Sun, Jiamei and Chong, Penny and Tan, Yi Xiang Marcus and Binder, Alexander}
}
```

### Acknowledgements
This work was generously supported by the ST Electronics-SUTD Cyber Security Laboratory. The authors express gratefulness for the ISTD-SUTD start-up funding.
