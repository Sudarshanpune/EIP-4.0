**Final Validation accuracy for Base Network**
Accuracy on test data is: 82.19

**Model definition (model.add... ) with output channel size and receptive field**
model = Sequential() model.add(SeparableConv2D(48, kernel_size=(3,3), input_shape=(32, 32, 3))) #30X30X48 #RF=3 model.add(BatchNormalization()) model.add(Activation('relu')) model.add(Dropout(0.05))

model.add(SeparableConv2D(48, kernel_size=(3,3))) #28X28X48 #RF=5 model.add(BatchNormalization()) model.add(Activation('relu')) #model.add(Dropout(0.2))

model.add(MaxPooling2D(pool_size=(2, 2))) #14X14X48 #RF=6

model.add(SeparableConv2D(64, kernel_size=(3,3), border_mode='same')) #12X12X96 #RF=10 model.add(BatchNormalization()) model.add(Activation('relu')) model.add(Dropout(0.2))

model.add(SeparableConv2D(96, kernel_size=(3,3))) #12X12X96 #RF=14 model.add(BatchNormalization()) model.add(Activation('relu')) #model.add(Dropout(0.2))

model.add(MaxPooling2D(pool_size=(2, 2))) #6X6X96 #RF=16 model.add(Dropout(0.2))

model.add(SeparableConv2D(128, kernel_size=(3,3), border_mode='same')) #4X4X192 #RF=24 model.add(BatchNormalization()) model.add(Activation('relu')) model.add(Dropout(0.2))

model.add(SeparableConv2D(192, kernel_size=(3,3))) #4X4X192 #RF=32 model.add(BatchNormalization()) model.add(Activation('relu')) model.add(Dropout(0.2))

model.add(MaxPooling2D(pool_size=(2, 2))) #2X2X192 #RF=36

model.add(SeparableConv2D(num_classes,kernel_size=(2,2))) #1X1X10 #RF=44 model.add(Flatten())

model.add(Activation('softmax'))

**50 Epoch logs**
Epoch 1/50
390/390 [==============================] - 30s 76ms/step - loss: 1.5209 - acc: 0.4465 - val_loss: 1.2825 - val_acc: 0.5341
Epoch 2/50
390/390 [==============================] - 27s 70ms/step - loss: 1.1245 - acc: 0.5960 - val_loss: 1.1123 - val_acc: 0.6069
Epoch 3/50
390/390 [==============================] - 27s 70ms/step - loss: 0.9901 - acc: 0.6456 - val_loss: 0.9543 - val_acc: 0.6657
Epoch 4/50
390/390 [==============================] - 27s 70ms/step - loss: 0.9071 - acc: 0.6779 - val_loss: 1.0206 - val_acc: 0.6450
Epoch 5/50
390/390 [==============================] - 27s 70ms/step - loss: 0.8386 - acc: 0.7047 - val_loss: 0.8983 - val_acc: 0.6822
Epoch 6/50
390/390 [==============================] - 27s 70ms/step - loss: 0.7826 - acc: 0.7227 - val_loss: 0.8116 - val_acc: 0.7228
Epoch 7/50
390/390 [==============================] - 27s 70ms/step - loss: 0.7419 - acc: 0.7364 - val_loss: 0.8481 - val_acc: 0.7119
Epoch 8/50
390/390 [==============================] - 27s 70ms/step - loss: 0.7138 - acc: 0.7482 - val_loss: 0.7095 - val_acc: 0.7580
Epoch 9/50
390/390 [==============================] - 27s 70ms/step - loss: 0.6801 - acc: 0.7592 - val_loss: 0.7923 - val_acc: 0.7366
Epoch 10/50
390/390 [==============================] - 27s 70ms/step - loss: 0.6578 - acc: 0.7691 - val_loss: 0.7232 - val_acc: 0.7504
Epoch 11/50
390/390 [==============================] - 27s 70ms/step - loss: 0.6407 - acc: 0.7746 - val_loss: 0.7019 - val_acc: 0.7574
Epoch 12/50
390/390 [==============================] - 27s 70ms/step - loss: 0.6201 - acc: 0.7795 - val_loss: 0.6939 - val_acc: 0.7688
Epoch 13/50
390/390 [==============================] - 27s 70ms/step - loss: 0.6041 - acc: 0.7867 - val_loss: 0.6679 - val_acc: 0.7720
Epoch 14/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5879 - acc: 0.7914 - val_loss: 0.6655 - val_acc: 0.7713
Epoch 15/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5729 - acc: 0.7976 - val_loss: 0.6498 - val_acc: 0.7784
Epoch 16/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5582 - acc: 0.8018 - val_loss: 0.6094 - val_acc: 0.7941
Epoch 17/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5429 - acc: 0.8081 - val_loss: 0.6097 - val_acc: 0.7947
Epoch 18/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5302 - acc: 0.8114 - val_loss: 0.6366 - val_acc: 0.7809
Epoch 19/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5284 - acc: 0.8123 - val_loss: 0.6551 - val_acc: 0.7731
Epoch 20/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5162 - acc: 0.8167 - val_loss: 0.6043 - val_acc: 0.7971
Epoch 21/50
390/390 [==============================] - 27s 70ms/step - loss: 0.5057 - acc: 0.8206 - val_loss: 0.6054 - val_acc: 0.7976
Epoch 22/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4984 - acc: 0.8231 - val_loss: 0.6534 - val_acc: 0.7733
Epoch 23/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4898 - acc: 0.8241 - val_loss: 0.7459 - val_acc: 0.7600
Epoch 24/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4823 - acc: 0.8301 - val_loss: 0.6268 - val_acc: 0.7883
Epoch 25/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4726 - acc: 0.8338 - val_loss: 0.6250 - val_acc: 0.7932
Epoch 26/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4684 - acc: 0.8325 - val_loss: 0.6010 - val_acc: 0.8012
Epoch 27/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4584 - acc: 0.8369 - val_loss: 0.6144 - val_acc: 0.7986
Epoch 28/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4508 - acc: 0.8397 - val_loss: 0.6111 - val_acc: 0.7961
Epoch 29/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4488 - acc: 0.8418 - val_loss: 0.5901 - val_acc: 0.7991
Epoch 30/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4413 - acc: 0.8427 - val_loss: 0.5464 - val_acc: 0.8190
Epoch 31/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4382 - acc: 0.8446 - val_loss: 0.6327 - val_acc: 0.7941
Epoch 32/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4265 - acc: 0.8479 - val_loss: 0.6067 - val_acc: 0.7947
Epoch 33/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4254 - acc: 0.8484 - val_loss: 0.5809 - val_acc: 0.8101
Epoch 34/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4167 - acc: 0.8502 - val_loss: 0.5588 - val_acc: 0.8127
Epoch 35/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4153 - acc: 0.8513 - val_loss: 0.5882 - val_acc: 0.8043
Epoch 36/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4104 - acc: 0.8534 - val_loss: 0.5355 - val_acc: 0.8245
Epoch 37/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4051 - acc: 0.8554 - val_loss: 0.5878 - val_acc: 0.8078
Epoch 38/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3991 - acc: 0.8575 - val_loss: 0.5542 - val_acc: 0.8164
Epoch 39/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3965 - acc: 0.8575 - val_loss: 0.5957 - val_acc: 0.8092
Epoch 40/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3940 - acc: 0.8584 - val_loss: 0.6333 - val_acc: 0.7929
Epoch 41/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3930 - acc: 0.8613 - val_loss: 0.5333 - val_acc: 0.8256
Epoch 42/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3803 - acc: 0.8629 - val_loss: 0.6107 - val_acc: 0.8094
Epoch 43/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3780 - acc: 0.8637 - val_loss: 0.5731 - val_acc: 0.8200
Epoch 44/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3804 - acc: 0.8639 - val_loss: 0.5883 - val_acc: 0.8078
Epoch 45/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3766 - acc: 0.8667 - val_loss: 0.5092 - val_acc: 0.8318
Epoch 46/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3710 - acc: 0.8671 - val_loss: 0.5344 - val_acc: 0.8247
Epoch 47/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3700 - acc: 0.8675 - val_loss: 0.5493 - val_acc: 0.8246
Epoch 48/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3645 - acc: 0.8700 - val_loss: 0.5904 - val_acc: 0.8164
Epoch 49/50
390/390 [==============================] - 27s 70ms/step - loss: 0.3606 - acc: 0.8705 - val_loss: 0.5760 - val_acc: 0.8163
Epoch 50/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3536 - acc: 0.8735 - val_loss: 0.5444 - val_acc: 0.8219
Model took 1365.24 seconds to train

Accuracy on test data is: 82.19
