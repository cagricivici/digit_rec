Character recognition with DL

First study:
----------- 
![Ekran Resmi 2020-01-02 01 12 36](https://user-images.githubusercontent.com/49865957/103447095-c2636a80-4c97-11eb-8692-84eba450fd84.png)

* importing cv2 and pillow
* difference btw them
* edge detection versus max_val and min_val


* plotting


Second study:
----------- 
![conversion](https://user-images.githubusercontent.com/49865957/101990919-3b375e00-3cba-11eb-9d58-4a8d5db6e6dc.jpg)

This step will serve to convert the visuals of all letters written in accordance with all the rules in the literature to text format.

Letter_Images folder: we need characters which contain pure pixels. Why pure pixels? Because this code control with test characters and orginal characters pixels by pixels. (only A, B and C be used - if needs, it can be increased)

Test_Images folder: characters which as a copy of original one. Why we put original characters into this folder, its answer is to control or compare pixels by pixels. Without ML, DL; if even there is a one pixel difference btw original and test letters, comparasion methods can result as 'false' in any case. (Therefore we need ML/DL solutions to tackle this problem.)

 If the letters written in the same format are compared to pixels, it can be determined which character is used. But pixel by pixel comparison is not a real-life method, so we need ML/DL solutions.

Third study:
----------- 
- import dataset from keras MNIST

![mnist](https://user-images.githubusercontent.com/49865957/103159547-cf85e280-47db-11eb-868b-38e8a6100699.png)


- train the model which would be able to recognize digits
- test model

This step contains Convolutional Neural Network (CNN) Structure. Because there is not any specific feature from some data. We need create features (feature vector) from each dataset. While training model, features will update according to dataset. Therefore, we need to use CNN. 

>Our model: 

Train(x_train, y_train) and test(x_test, y_test) dataset is downloaded from mnist sources.
x_train has 60k images. y_train is a value cluster of x_train as a number. But this point is crucial; y_train dataset contains digits such as 2,3,4. To categorization, we need to use **one_hot_encoding** transformation. With help of this transformation, the result of model will assign tocorrect place.

To test training model, 10000 images exist in t_test and values of x_test as a number is in y_test. 

After test run, only one result occurs such as %xx accuracy. This is a result which training model applied on test dataset.

- 4 Layers -50 50 50 10 neurons - shown as model_plot.png 
-Activation variety: tanh, relu and softmax
- 0.5 drop-out applied on model to avoid of overfitting
- loss function = 'categorical_crossentropy'
- Validation split: 0.1 * x_train
- metrics: validation accuracy, validation loss, test accuracy and test loss


**Test Accuracy: 94.90%**
