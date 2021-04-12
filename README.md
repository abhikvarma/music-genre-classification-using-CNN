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
* As these spectrograms are images, we can treat this as an immage classification problem
* We train a CNN to classify these spectrograms into their genres
* ![CNN model summary](https://user-images.githubusercontent.com/43804297/114367304-f0f7b800-9b99-11eb-8f6f-6fd8d5b72305.png)
* Training information:
* ![Training Info](https://user-images.githubusercontent.com/43804297/114367926-901caf80-9b9a-11eb-8f2b-8796ce95b03f.png)

