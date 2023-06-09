## Ways to improve the model:

### Image Augmentation

Image Augmentation is a very simple, but very powerful tool to help you avoid overfitting your data. The concept is very simple though: If you have limited data, then the chances of you having data to match potential future predictions is also limited, and logically, the less data you have, the less chance you have of getting accurate predictions for data that your model hasn't yet seen. To put it simply, if you are training a model to spot cats, and your model has never seen what a cat looks like when lying down, it might not recognize that in future.

Augmentation simply amends your images on-the-fly while training using transforms like rotation. 
So, it could 'simulate' an image of a cat lying down by rotating a 'standing' cat by 90 degrees. As such you get a cheap way of extending your dataset beyond what you have already. 

To learn more about Augmentation, and the available transforms, check out 
https://keras.io/api/layers/preprocessing_layers/
 -- and note that it's referred to as preprocessing for a very powerful reason: that it doesn't require you to edit your raw images, nor does it amend them for you on-disk. It does it `in-memory` as it's performing the training, allowing you to experiment without impacting your dataset. 
 
 Src: https://www.coursera.org/learn/convolutional-neural-networks-tensorflow/supplement/I8qgl/image-augmentation


### Using dropout!
Another useful tool to explore at this point is the Dropout. 

The idea behind it is to remove a random number of neurons in your neural network. This works very well for two reasons: The first is that neighboring neurons often end up with similar weights, which can lead to overfitting, so dropping some out at random can remove this. The second is that often a neuron can over-weigh the input from a neuron in the previous layer, and can over specialize as a result. Thus, dropping out can break the neural network out of this potential bad habit! 

Check out Andrew's terrific video explaining dropouts here: 
https://www.youtube.com/watch?v=ARq74QuavAo

Src: https://www.coursera.org/learn/convolutional-neural-networks-tensorflow/supplement/GtDVB/using-dropout



