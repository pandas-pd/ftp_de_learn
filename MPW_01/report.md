# Mandatory Practical Work 01 - Report

## Group

- Student 1 : Piu, Maurizio
- Student 2 : Tauss, Joël

## Goal

The goal is to

- apply the concepts seen in the lectures and practical sessions,
- and to document your experimentation process and results in a report.

The report should be clear, concise, and well-structured, and should include all relevant details about your experiments, including the
hyperparameters you used, the results you obtained, and any insights or conclusions you can draw from your experiments.

## Objectives

### Mandatory Objectives

- [x] Start from simple CNN architectures and progressively increase their complexity to show the benefit of depth.
- [x] Show the importance of hyperparameter tuning. (lr, batch_size, epochs, layers&units, regularisation params)
- [x] Show models that overfit and underfit and explain the reasons for that.
- [x] Experiment with regularization techniques.
- [x] Experiment with different optimization algorithms (e.g., Adam, RMSprop) and compare their performance.


Hint : Resizing the images e.g., 128x128 or 64x64 may be useful at the beginning of your investigations to perform quicker experimentations and sweep towards good settings.

### Optional objectives

Pick at least 2 of the following optional objectives to further explore and analyze the performance of your models:

Picked objectives:

- [x] CHOICE-M: Experiment with data augmentation techniques to improve model generalization (e.g.,random cropping, horizontal flipping, color jittering).
- [x] Perform transfer learning using pre-trained models and compare their performance with models trained from scratch.
- [x] Augment the dataset by re-collecting images (e.g., using the Bing API with image-scraper.py) ; use your best model to validate the newly collected images.
- [ ] Use tools to monitor the training process and analyze the training and validation curves (e.g., Tensorboard, Weights & Biases).

Possible objectives:

- Manually inspect misclassifications of your best model to identify mis-labelled samples in the dataset. Analyze their impact on model performance (i.e. when they are removed from the training set, when they are removed from the validation set, when they are kept in both sets). If you do so, provide logs of the mis-labelled images.

- Use frameworks to automatically search for the best hyperparameters (e.g., Optuna, Hyperopt) and compare their performance with manual tuning.
- Use advanced architectures (e.g., ResNet, DenseNet) and compare their performance with simpler architectures.
- Augment the dataset by re-collecting images (e.g., using the Bing API with image-scraper.py) ; use your best model to validate the newly collected images.
- Use visualization techniques (e.g., Grad-CAM) to understand which parts of the images the model is focusing on when making predictions.

## Dataset

We will use the iCoSimal V3 dataset that contains 30’000 images of animals in 10 categories.

It has the following characteristics :

- Number of classes : 10
- Number of images : 30’000
- Image resolution : 224x224 pixels
- Split : 24’000 training images, 6’000 ’validation’ images (to be used as the test set)
- Class distribution : Balanced
- Classes : cat, chicken, cow, dog, elephant, horse, rabbit, sheep, squirrel, zebra
- Source of images : Collected from direct downloads from the net (using Bing API) and various open-source image repositories including Coco and OpenImages v7 datasets.
- Grooming : to avoid duplicates and prepare the sets, image-groomer.py was used


---
# Notes from lecture 2026-04-01

- Fix the model and only change one param to see how the model behaves (controlled experiment)
    - 2 to 3 such experiment per group memeber
    - e.g. learning rate, optimizer, optimizer params, nodes for layers, dropout reate, epochs, etc.
- Expectation: Run Trainings with many number of epochs (overnight):
    - You may reduce image size to do so (already done)
- Try not compressing the data to achieve better performance


