## Computer vision app to predict Pneumonia from chest X-ray using deep neural network

Dataset    : [Dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia)<br/>
Framework  : [Tensorflow v2.x](https://www.tensorflow.org/)<br/>
#Training  : 5216<br/>
#Testing   : 624<br/>


### Architecture : Modified [LeNet5](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf)

**Layer 1** : CNN (filters = 8, kernel_size = (5,5), activation = Relu, strides = (5,5), padding = Same)<br/>
**Layer 2** : AveragePool(pool_size = (2,2))

**Layer 3** : CNN (filters = 10, kernel_size = (5,5), activation = Relu, strides = (0,0), padding = Valid)<br/>
**Layer 4** : AveragePool(pool_size = (2,2)) 

**Layer 5** : Flatten<br/>

**Layer 6** : Dense(120, activation= Relu)<br/>
**Layer 7** : Dense(84, activation= Relu)<br/>
**Layer 8** : Dense(1, activation= Sigmoid)<br/>

**Cost Function** : Binary Cross entropy<br/>
**Optimization** : Adam's Optimization<br/>

| Epoch       | Train Accuracy           | Test Accuracy  | Train Loss |
| ------------- |:-------------:| -----:| -----------:|
| 100 | 0.9649      |    0.9647 | 0.0955 |
| 75     | 0.9590 | 0.9599 | 0.1050 |
| 50      | 0.9298      |   0.9323| 0.1689 |
| 25 | 0.8825      |    0.8982 | 0.2691 |

### Epoch to loss/accuracy graph for 100 epochs
![Loss/Accuracy/100Epoch](https://github.com/MaitreyPrajapati/pneumonia_detection/blob/master/Graph/100Epoch.png)

### Epoch to accuracy graph for 75 epochs
![Loss/Epoch](https://github.com/MaitreyPrajapati/pneumonia_prediction/blob/master/Graph/75epoch.jpeg)




