**20 Epochs**

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 31s 512us/step - loss: 0.0353 - acc: 0.9853 - val_loss: 0.0268 - val_acc: 0.9937
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 11s 188us/step - loss: 0.0329 - acc: 0.9851 - val_loss: 0.0274 - val_acc: 0.9931
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 11s 185us/step - loss: 0.0304 - acc: 0.9852 - val_loss: 0.0221 - val_acc: 0.9943
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 11s 184us/step - loss: 0.0285 - acc: 0.9858 - val_loss: 0.0255 - val_acc: 0.9941
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 11s 184us/step - loss: 0.0285 - acc: 0.9859 - val_loss: 0.0233 - val_acc: 0.9939
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 11s 183us/step - loss: 0.0257 - acc: 0.9877 - val_loss: 0.0200 - val_acc: 0.9941
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 11s 184us/step - loss: 0.0256 - acc: 0.9875 - val_loss: 0.0251 - val_acc: 0.9935
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0256 - acc: 0.9874 - val_loss: 0.0257 - val_acc: 0.9934
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0264 - acc: 0.9867 - val_loss: 0.0233 - val_acc: 0.9941
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 11s 183us/step - loss: 0.0238 - acc: 0.9878 - val_loss: 0.0231 - val_acc: 0.9939
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 11s 181us/step - loss: 0.0248 - acc: 0.9873 - val_loss: 0.0236 - val_acc: 0.9942
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0245 - acc: 0.9875 - val_loss: 0.0207 - val_acc: 0.9944
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0237 - acc: 0.9874 - val_loss: 0.0218 - val_acc: 0.9945
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0249 - acc: 0.9876 - val_loss: 0.0212 - val_acc: 0.9946
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0233 - acc: 0.9881 - val_loss: 0.0225 - val_acc: 0.9941
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 11s 181us/step - loss: 0.0227 - acc: 0.9877 - val_loss: 0.0227 - val_acc: 0.9946
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 11s 181us/step - loss: 0.0216 - acc: 0.9884 - val_loss: 0.0221 - val_acc: 0.9947
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 11s 183us/step - loss: 0.0227 - acc: 0.9880 - val_loss: 0.0216 - val_acc: 0.9947
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 11s 183us/step - loss: 0.0226 - acc: 0.9877 - val_loss: 0.0218 - val_acc: 0.9947
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 11s 182us/step - loss: 0.0229 - acc: 0.9876 - val_loss: 0.0214 - val_acc: 0.9948


**model.evaluate (on test data)**
[0.021420345493074002, 0.9948]



**Strategy**
1. To remove bias value, should include "bias=false" in our code.
2. To reduce parameters within limits, I have reduced the number of channels in convolutional layer2 from 32 to 16 and layer7 from 16 to 10.
3. Parametes reducced to 11.7K and got accuracy 99.48%
4. I have reduced droupout from 0.1 to 0.05
