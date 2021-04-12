# music-genre-classification-using-CNN

## libraries
* Tensorflow
* Matplotlib
* Librosa
* Numpy
* Pandas

## dataset
* [fma_small](https://os.unil.cloud.switch.ch/fma/fma_small.zip "fma_small download link")
  * 8,000 tracks of 30s, 8 balanced genres (7.2gb)

## methodoloy
* Mel Spectrograms were created from the first 10 seconds of each song in the dataset
* ![Example of Mel Spectrogram](https://user-images.githubusercontent.com/43804297/114368356-fbff1800-9b9a-11eb-9962-8b429d16c291.png)
* As these spectrograms are images, we can treat this as an immage classification problem
* We train a CNN to classify these spectrograms into their genres
* ![CNN model summary](https://user-images.githubusercontent.com/43804297/114367304-f0f7b800-9b99-11eb-8f6f-6fd8d5b72305.png)

## training
* An adam optimizer was used for training
* Categorical Crossentropy loss was used since it was a classification problem
* We noticed overfitting, to reduce this we
  * Removed instrumental songs from our data since it showed the highest misclassification
  * Reduced complexity of our CNN model
  * Added regularization and a dropout layer
* We got the following Accuracy and Loss graphs (blue = validation | orange = training)
* ![Accuracy graph](https://user-images.githubusercontent.com/43804297/114369085-a8d99500-9b9b-11eb-9a63-3a911844dc6e.png)
* ![Loss graph](https://user-images.githubusercontent.com/43804297/114369101-ac6d1c00-9b9b-11eb-8e6f-9e11a0196d69.png)

