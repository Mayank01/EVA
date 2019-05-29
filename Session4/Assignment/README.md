# Architectural Basics :
### 1. How many layers : 
  >a. ***we have using MNIST DATA set which has image size 28x28 so initial in layers we easily gets important features***.
  
  >b. ***Now we gets all Neccesary features Before Max pooling, first channel size 16 and second one 32 to get edges and gradient in image size 28x28***
  
### 2. Max Pooling :
  >c. ***MaxPooling carry forward important features only, as we already gets important information***
  
  >d. ***Max Pooling reduce Dimensionality(no. of layers) too which ease Calculation once you get neccesary Information from input image***
  
### 3. 1x1 ***ANT MAN***:
 >e. ***1x1 helps to reduce no. of channels or depth of network, without impacting features of model*** 
 
 >f. ***1x1 wont increase images count, it only helps to louder features voice with decrease channel size or it wont differentiate or mix multiple features,pixel to get new information, it uses existing information only to higher the amplitude***.

### 4. 3x3 Convolution:
 >g. ***Here we use 3x3 before maxpooling to get all edges, gradient, and after max pooling to get parts of objects with forward layers in network***.
 
 >h. ***we used 3x3 to extract important features from input image, it has symmetry which helps to align all pixels and get neccesary information***.

### 5. Receptive Field:
 >i. ***RF getting after every layers of convolution. its increases by 2 with convolution and doubling at maxpooling layer***.
 
 >j. ***As input region space that particular kernal feature looking at called RF***.

### 6. SoftMax:
 >k. ***Its kind of Activation function which used at last layer of prediction to get distributed probabilistic result***.
 
 >l.***it helps network to predict better with classified domain***.

### 7. Learning Rate:
 >m. ***LR is part of Training the model, its as steps size taken by network to learn information with updating weights. Fixed learning rate is not good for model. Start with larger LR to accomodate larger changes in initial weights of model to get fine tuning in later stage and decrease accordingly*** 

     
### new_weight = existing_weight — learning_rate * gradient
![alt text](https://cdn-images-1.medium.com/max/900/0*00BrbBeDrFOjocpK.)


### 8.Kernels and how do we decide the number of kernels:
 >n. ***Its depend on Task or Dataset which we work on, its intutievly we decide as complex features we must n should break features to ,larger channels so larger kernals needed, if easy dataset than less kernals do best job***.


### 9. Position of Maxpooling:
 >o. ***Once you get all important features then apply max pooling to reduce dimension and extract main features***.
 
 >p. ***like in this network after 2 layers i got most important features then applied MP***.
 
### 10. Transitional Layer:
 >q. ***After Convolution Layer we put Transition layer where we using "Maxpooling + 1x1" to change network depth and channel dimension***.
 
### 11. Position of Transition layer:
 >r. ***Here i used Max pooling after 1x1 because 1x1 helps to increase features voice individually and post MP helps to extract those information gives network gain/edge to learn.***
 
### 12. no. of Epochs & when to increase them:
 >1. ***No. of epochs has relation with learning rate and hope to get good validation accuracy***.
 
 >2. ***when model getting underfitting/ there is small gap btw train_acc and val_acc then epochs will helps to get increase validation accuracy as there is hope***.
 
### 13. DropOut:
 >1. ***Dropouts is a regularization technique, which helps to learn kernal more features by dropping random layers of model in training proccess to prevent overfitting***.
 
### 14. when we introduce dropout:
 >1. ***When model performing well in training accuracy but not able get good accuracy in validation, our network shows overfitting***.
 
 >2. ***So expilictly dropping some random layers pixel pressurize kernal to learn more with other pixel layers which reduce overfitting and model perform well.***
 
### 15. The distance of MaxPooling from Prediction:
 >1. ***we do first maxpooling once we get neccesary edges and gradient then after some convolution layer we get textures, pattern then we do max pooling***.
 
 >2. ***MP reduce dimensionality and drop important features/pixels, so to regain model with proper information we should not do max pooling with short interval. and distance between Maxpooling and Prediction be more to ragain model all important object, parts of objects information to predict better results.***
 
### 16. The distance of Batch Normalization from Prediction:
 >1.***BatchNorms will helps to intialize weights batchwise using means, variance of channels to give better results***.
 
 >2.***It doesn't matter distance for BN with prediction layer as Backprop take care of arranging/handle as per there need***.
 
### 17.When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered):
 >1. ***first assumution, Once you get RF equals size of image you should stop***
 
 >2. ***Other is you get all Important features or objects or parts of object to do prediction you should stop Convolution***.
 
 >3. ***Larger Kernal size use at last layer before prediction where We sure as achieve better RF with we go head and use 3x3, 7x7,4x4 etc***.
 
### 18. How do we know our network is not going well, comparatively, very early:
 >1. ***By checking early Training accuracy as its shows where our final accuracy or model will go***.
 
 >2. ***We can change batch size learning rate to help model to perform well while training model***
 
### 19.Batch Size, and effects of batch size:
 >1. ***Larger the Batch size helps to train model faster but do not converge faster always***.
 
 >2. ***Smaller the Batch size will train/progress model slower but converges faster as its all depend on Problem***.
 
 >3. ***Ideal Batch size would be 32 or 64***.
 
### 20.When to add validation checks:
 > 1.***Validation Set used to minimize overfitting or where we should stop training***
 
 > 2.***Validation check put while training the model to check network performing well on validation same as training if not we need to do something***.
 
***Training Set***: this data set is used to adjust the weights on the neural network.

***Validation Set***: this data set is used to minimize overfitting. You're not adjusting the weights of the network with this data set, you're just verifying that any increase in accuracy over the training data set actually yields an increase in accuracy over a data set that has not been shown to the network before, or at least the network hasn't trained on it (i.e. validation data set). If the accuracy over the training data set increases, but the accuracy over the validation data set stays the same or decreases, then you're overfitting your neural network and you should stop training.

***Testing Set***: this data set is used only for testing the final solution in order to confirm the actual predictive power of the network.

### 22. LR schedule and concept behind it:
>1. ***LR update weights during the training process, the amount in which they update called scheduled or steps sizes***.

>2. ***Keras support LR schedule: The way in which the learning rate changes over time (training epochs) is referred to as the learning rate schedule or learning rate decay***

>3. ***We need to converge Slowly and steady with based LR so we used Schedule or adaptive***.

[Source LR](https://machinelearningmastery.com/learning-rate-for-deep-learning-neural-networks/)

[Source LR](https://machinelearningmastery.com/understand-the-dynamics-of-learning-rate-on-deep-learning-neural-networks/)

[Source LR](https://developers.google.com/machine-learning/crash-course/reducing-loss/learning-rate)

![alt text](https://cdn-images-1.medium.com/max/900/0*uIa_Dz3czXO5iWyI.)

### 23. Adam vs SGD:
>1. ***Optimization algorithm main objective to reduce error rate while training the model***.

>***There are two metrics to determine the efficacy of an optimizer:***
>1. ***speed of convergence (the process of reaching a global optimum for gradient descent)***.

>2. ***generalization (the model’s performance on new data)***

>3. ***Adam:*** Helps to covergence faster, computes individual adaptive learning rates for different parameters

>4. ***SGD is variant of gradient descent.*** Instead of performing computations on the whole dataset — which is redundant and inefficient — SGD only computes on a small subset or random selection of data examples. SGD produces the same performance as regular gradient descent when the learning rate is low

[Compare AdamvsSGD](https://medium.com/syncedreview/iclr-2019-fast-as-adam-good-as-sgd-new-optimizer-has-both-78e37e8f9a34)

### 24. Image normalization:
>1. ***Image normalization is stretching of pixel values, contrasting images to improve pixel intensity***.

>2. ***it helps model to train faster with less no. of iteration and reduce loss***.
