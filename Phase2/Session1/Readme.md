# Using an Embedding layer & Classifier on the IMDB data
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:541: The name tf.placeholder is deprecated. Please use tf.compat.v1.placeholder instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:4432: The name tf.random_uniform is deprecated. Please use tf.random.uniform instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/optimizers.py:793: The name tf.train.Optimizer is deprecated. Please use tf.compat.v1.train.Optimizer instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:3657: The name tf.log is deprecated. Please use tf.math.log instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/tensorflow_core/python/ops/nn_impl.py:183: where (from tensorflow.python.ops.array_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use tf.where in 2.0, which has the same broadcast rule as np.where
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param    
=================================================================
embedding_2 (Embedding)      (None, 20, 8)             80000     
_________________________________________________________________
flatten_1 (Flatten)          (None, 160)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 161       
=================================================================
Total params: 80,161
Trainable params: 80,161
Non-trainable params: 0
_________________________________________________________________
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:1033: The name tf.assign_add is deprecated. Please use tf.compat.v1.assign_add instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:1020: The name tf.assign is deprecated. Please use tf.compat.v1.assign instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:3005: The name tf.Session is deprecated. Please use tf.compat.v1.Session instead.

Train on 20000 samples, validate on 5000 samples
Epoch 1/10
WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:190: The name tf.get_default_session is deprecated. Please use tf.compat.v1.get_default_session instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:197: The name tf.ConfigProto is deprecated. Please use tf.compat.v1.ConfigProto instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:207: The name tf.global_variables is deprecated. Please use tf.compat.v1.global_variables instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:216: The name tf.is_variable_initialized is deprecated. Please use tf.compat.v1.is_variable_initialized instead.

WARNING:tensorflow:From /usr/local/lib/python3.6/dist-packages/keras/backend/tensorflow_backend.py:223: The name tf.variables_initializer is deprecated. Please use tf.compat.v1.variables_initializer instead.

> 20000/20000 [==============================] - 2s 108us/step - loss: 0.6743 - acc: 0.6108 - val_loss: 0.6317 - val_acc: 0.6858
> Epoch 2/10

> 20000/20000 [==============================] - 2s 80us/step - loss: 0.5514 - acc: 0.7525 - val_loss: 0.5318 - val_acc: 0.7240
> Epoch 3/10

> 20000/20000 [==============================] - 2s 82us/step - loss: 0.4635 - acc: 0.7887 - val_loss: 0.5041 - val_acc: 0.7406
> Epoch 4/10

> 20000/20000 [==============================] - 2s 81us/step - loss: 0.4205 - acc: 0.8112 - val_loss: 0.4979 - val_acc: 0.7472
> Epoch 5/10

> 20000/20000 [==============================] - 2s 83us/step - loss: 0.3907 - acc: 0.8285 - val_loss: 0.4983 - val_acc: 0.7506
> Epoch 6/10

> 20000/20000 [==============================] - 2s 84us/step - loss: 0.3659 - acc: 0.8406 - val_loss: 0.5013 - val_acc: 0.7510
> Epoch 7/10

> 20000/20000 [==============================] - 2s 82us/step - loss: 0.3432 - acc: 0.8537 - val_loss: 0.5076 - val_acc: 0.7524
> Epoch 8/10

> 20000/20000 [==============================] - 2s 82us/step - loss: 0.3227 - acc: 0.8643 - val_loss: 0.5135 - val_acc: 0.7514
> Epoch 9/10

> 20000/20000 [==============================] - 2s 81us/step - loss: 0.3032 - acc: 0.8752 - val_loss: 0.5220 - val_acc: 0.7498
> Epoch 10/10

> 20000/20000 [==============================] - 2s 83us/step - loss: 0.2846 - acc: 0.8854 - val_loss: 0.5327 - val_acc: 0.7462

## Loading pretrained word embeddings into the Embedding layer
### Train on 8000 samples, validate on 10000 samples
> Epoch 1/10
> 8000/8000 [==============================] - 3s 343us/step - loss: 0.8235 - acc: 0.5902 - val_loss: 0.6494 - val_acc: 0.6503

> Epoch 2/10
> 8000/8000 [==============================] - 2s 296us/step - loss: 0.6281 - acc: 0.6894 - val_loss: 0.8926 - val_acc: 0.5798

> Epoch 3/10
> 8000/8000 [==============================] - 2s 291us/step - loss: 0.5276 - acc: 0.7464 - val_loss: 0.6005 - val_acc: 0.7001

> Epoch 4/10
> 8000/8000 [==============================] - 2s 305us/step - loss: 0.4419 - acc: 0.7902 - val_loss: 0.6422 - val_acc: 0.6925

> Epoch 5/10
> 8000/8000 [==============================] - 2s 303us/step - loss: 0.3797 - acc: 0.8271 - val_loss: 0.6796 - val_acc: 0.6895

> Epoch 6/10
> 8000/8000 [==============================] - 2s 300us/step - loss: 0.3341 - acc: 0.8536 - val_loss: 0.7225 - val_acc: 0.6913

> Epoch 7/10
> 8000/8000 [==============================] - 2s 304us/step - loss: 0.2904 - acc: 0.8762 - val_loss: 0.7260 - val_acc: 0.6924

> Epoch 8/10
> 8000/8000 [==============================] - 2s 301us/step - loss: 0.2506 - acc: 0.8951 - val_loss: 0.7821 - val_acc: 0.6840

> Epoch 9/10
> 8000/8000 [==============================] - 2s 289us/step - loss: 0.2127 - acc: 0.9154 - val_loss: 0.8244 - val_acc: 0.6855

> Epoch 10/10
> 8000/8000 [==============================] - 2s 310us/step - loss: 0.1788 - acc: 0.9285 - val_loss: 0.9668 - val_acc: 0.6742

![alt text](https://github.com/Aspire-Mayank/EVA/blob/master/Phase2/Session1/pre_trainedWordEmbedding.PNG)

## Training the same model without pretrained word Embeddings
### Train on 8000 samples, validate on 10000 samples
> Epoch 1/10
> 8000/8000 [==============================] - 6s 710us/step - loss: 0.5397 - acc: 0.7225 - val_loss: 0.3986 - val_acc: 0.8196

> Epoch 2/10
> 8000/8000 [==============================] - 5s 672us/step - loss: 0.1355 - acc: 0.9577 - val_loss: 0.4397 - val_acc: 0.8137

> Epoch 3/10
> 8000/8000 [==============================] - 5s 645us/step - loss: 0.0089 - acc: 0.9989 - val_loss: 0.5875 - val_acc: 0.8115

> Epoch 4/10
> 8000/8000 [==============================] - 5s 640us/step - loss: 4.7153e-04 - acc: 1.0000 - val_loss: 0.7292 - val_acc: 0.8128

> Epoch 5/10
> 8000/8000 [==============================] - 5s 639us/step - loss: 2.4768e-05 - acc: 1.0000 - val_loss: 0.8535 - val_acc: 0.8116

> Epoch 6/10
> 8000/8000 [==============================] - 5s 658us/step - loss: 3.1011e-07 - acc: 1.0000 - val_loss: 0.9498 - val_acc: 0.8091

> Epoch 7/10
> 8000/8000 [==============================] - 5s 662us/step - loss: 1.1420e-07 - acc: 1.0000 - val_loss: 0.9832 - val_acc: 0.8122

> Epoch 8/10
> 8000/8000 [==============================] - 5s 667us/step - loss: 1.1063e-07 - acc: 1.0000 - val_loss: 0.9921 - val_acc: 0.8137

> Epoch 9/10
> 8000/8000 [==============================] - 5s 639us/step - loss: 1.1004e-07 - acc: 1.0000 - val_loss: 1.0019 - val_acc: 0.8124

> Epoch 10/10
> 8000/8000 [==============================] - 5s 663us/step - loss: 1.0996e-07 - acc: 1.0000 - val_loss: 1.0015 - val_acc: 0.8140

![alt text](https://github.com/Aspire-Mayank/EVA/blob/master/Phase2/Session1/WithoutPre-trainedWordEmbedding.PNG)

## Evaluating the model on the test data (using the pretrained word embeddings)
> 25000/25000 [==============================] - 1s 53us/step
> [0.9389304766702652, 0.67812]



#### DOWNLOADING THE GLOVE WORD EMBEDDINGS
##### Go to https://nlp.stanford.edu/projects/glove
Download the precomputed embeddings from 2014 English Wikipedia. It’s an 822 MB zip file called glove.6B.zip, containing 100-dimensional embedding vectors for 400,000 words (or nonword tokens). Unzip it
PREPROCESSING THE EMBEDDINGS
Let’s parse the unzipped file (a .txt file) to build an index that maps words (as strings) to their vector representation (as number vectors).

##### Please Follow book of page from 182-195 [Mention book] (http://faculty.neu.edu.cn/yury/AAI/Textbook/Deep%20Learning%20with%20Python.pdf)

## Keep Learning Keep Growing :)
