20 Epochs

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 12s 192us/step - loss: 0.4157 - acc: 0.9029 - val_loss: 0.0853 - val_acc: 0.9842
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 99us/step - loss: 0.1759 - acc: 0.9554 - val_loss: 0.0543 - val_acc: 0.9883
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 99us/step - loss: 0.1382 - acc: 0.9658 - val_loss: 0.0501 - val_acc: 0.9884
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 6s 100us/step - loss: 0.1163 - acc: 0.9703 - val_loss: 0.0393 - val_acc: 0.9906
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 6s 100us/step - loss: 0.1016 - acc: 0.9735 - val_loss: 0.0328 - val_acc: 0.9911
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0885 - acc: 0.9770 - val_loss: 0.0323 - val_acc: 0.9918
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0805 - acc: 0.9788 - val_loss: 0.0312 - val_acc: 0.9920
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 101us/step - loss: 0.0746 - acc: 0.9802 - val_loss: 0.0247 - val_acc: 0.9930
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 6s 101us/step - loss: 0.0681 - acc: 0.9806 - val_loss: 0.0291 - val_acc: 0.9926
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 6s 105us/step - loss: 0.0652 - acc: 0.9807 - val_loss: 0.0243 - val_acc: 0.9926
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 6s 103us/step - loss: 0.0611 - acc: 0.9812 - val_loss: 0.0230 - val_acc: 0.9934
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 6s 101us/step - loss: 0.0584 - acc: 0.9830 - val_loss: 0.0299 - val_acc: 0.9920
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 6s 103us/step - loss: 0.0559 - acc: 0.9827 - val_loss: 0.0217 - val_acc: 0.9940
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 6s 106us/step - loss: 0.0535 - acc: 0.9829 - val_loss: 0.0199 - val_acc: 0.9945
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 6s 106us/step - loss: 0.0509 - acc: 0.9837 - val_loss: 0.0203 - val_acc: 0.9936
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 6s 103us/step - loss: 0.0501 - acc: 0.9832 - val_loss: 0.0242 - val_acc: 0.9927
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 6s 103us/step - loss: 0.0471 - acc: 0.9844 - val_loss: 0.0180 - val_acc: 0.9951
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0463 - acc: 0.9846 - val_loss: 0.0213 - val_acc: 0.9946
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0455 - acc: 0.9842 - val_loss: 0.0184 - val_acc: 0.9946
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 6s 101us/step - loss: 0.0423 - acc: 0.9860 - val_loss: 0.0185 - val_acc: 0.9947

model.evaluate (on test data)
[0.018498290636902674, 0.9947]

Strategy
Firstly, we need to remove bias value. To do so, we include "bias=False" in our code
Then we need to reduce our parameters from 16.5k to below 15k.
For this I have reduce the no. channels in convolutional layer 2 from 32 to 16.
after this, the no of parameter are 13.6k
Next, the difference between validation accuracy and training accuracy was too large, I have reduced the value of dropout from 0.1 to 0.05
I tried to reduce batchsize from 128 to 64, but this actually reduces the accuracy so therefore I have set the batch value to 128
