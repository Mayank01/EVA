# GradCam Integration with Existing Model:
GradCam tells where CNN looking..
Defination : Gradient-weighted Class Activation Mapping (Grad-CAM), uses the gradients of any target concept (say logits for ‘dog’ or even a caption), flowing into the final convolutional layer to produce a coarse localization map highlighting the important regions in the image for predicting the concept.
> GradCam technique is not only useful for localization but it also used for Visual Question and Answering, Image captioning etc., as mentioned in their paper itself.

Also, it is very much helpful in debugging about the data requirements for building an accurate model. Though hyperparameter tuning is not much associated with this, we can generalize the model better with extra data and data augmentation techniques.

# About Cutout / Random Erasing
Cutout or Random Erasing is a kind of image augmentation methods for convolutional neural networks (CNN). They are very similar methods and were proposed almost at the same time.

They try to regularize models using training images that are randomly masked with random values.
