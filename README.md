# <div align="center">Detection of pneumonia on X-Rays</div>

### Binary classification

Firstly, I have attempted to train ResNet152 CNN without weights, using Tensorflow. I've obtained accuracy = 0.92 on the train dataset, accuracy = 0.89 on the validation dataset. Recall - 0.88. It meaned overfitting.

Further, I've decided to apply another approach and used PyTorch.
I chose ResNet50 with weights, freezed all the layers and added linear classifier (with 2 outputs). It took only 10 epochs to get enough good results.

Results achieved: train acc = 0.94, validation acc = 0.97, test acc = 0.95. Precision = 0.97, Recall = 0.97.

Thus, it turned out to increase Recall from 0.88 to 0.97 using transfer learning. FalseNegatives have been reduced from 44 to 25. 

Used image dataset from Kaggle: [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). I have applied the only one augmentation: RandomHorizontalFlip.

I have prepared train, val and test datasets in <a href="http:/roboflow.com/" rel="some text">![Foo](https://a.radikal.ru/a40/2202/6a/bdf9b3256872.png)</a>.

## <div align="center">Some test images: </div>

![The first test sample image](https://github.com/Kuaranir/Detection-of-pneumonia-on-X-Rays/blob/main/test-sample-1.png)
![The second test sample image](https://github.com/Kuaranir/Detection-of-pneumonia-on-X-Rays/blob/main/test-sample-2.png)
![The third test sample image](https://github.com/Kuaranir/Detection-of-pneumonia-on-X-Rays/blob/main/test-sample-3.png)

# <div align="center">Confusion matrix:</div>

![Confusion matrix](https://github.com/Kuaranir/Detection-of-pneumonia-on-X-Rays/blob/main/confusion_matrix.png)

This is my train pet-project.
