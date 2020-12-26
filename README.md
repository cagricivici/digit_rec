Character recognition with DL

First study:
----------- 
* importing cv2 and pillow
* difference btw them
* edge detection
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
- train the model which would be able to recognize digits
- test model

This step contains Convolutional Neural Network (CNN) Structure. Because there is not any specific feature from some data. We need create features (feature vector) from each dataset. While training model, features will update according to dataset. Therefore, we need to use CNN. 

