# convnets (with Keras)
3 different types of convolutional neural networks to classify cats and dogs
## 3 different models
### Model from scratch
This model is created from nothing. It contains 4 Convolutional layers, each of them followed by a MaxPooling. The model then flattens the result and passes it through a dense layer to final give to the final sigmoid layer. This model uses Data Augmentation and a dropout (right after flattening the last convolutional layer) to avoid overfitting.
### Using a pretrained model without Data Augmentation
This model uses the pretrained VGG16 for convolutional, but add its own dense layers (same of the previous one). It does not uses Data Augmentation. None of the weights of the VGG16 model are modified.
### Using a pretrained model with Data Augmentation
This model is based on the previous one, but allows for Data Augmentation. The weights of the last layers of VGG16 are modified (block 5, containing 3 convolutional layers and 1 MaxPooling).
