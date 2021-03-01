# Dog Breed classifier using CNN
The aim of the project is to build a pipeline to process real-world user-supplied images. The algorithm is expected to identify dog's breed with certain level of accuracy for a given image and if a human image is passed to it, it will try to predict the closest matching dog breed. If the algorithm is not able to predict human or dog then an error will be returned. Evaluate a model to detect dog breeds, humans and subsequently classify dog breeds that resembles humans.

---
# 1. Datasets
Two datasets provide by Udacity were used for this project and these are available at following AWS S3 locations for reference:
1. Human Dataset: https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip
2. Dog Dataset: https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip

---
# 2. Model selection
Chain of models were used for this problem to identify humans, identify dogs and subsequenty identify dog breeds for dogs and resembling dog breed for human. 
Detect Humans: Pre-trained OpenCV's implementation of Haar feature-based cascade classifiers 
Detect Dogs: Pre-trained VGG-16 Model
Detect Dog Breed: CNN model from scratch and CNN model (ResNet50) were trained using GPU acceleration

---
# 3. Model training
1. CNN model from scratch was trained using GPU acceleration for 20 epochs to achieve test accuracy of >=10%
2. CNN model using pre-trained ResNet50 model with Transfer learning was trained using GPU acceleration for 10 epochs to achieve test accuracy of >=60%

---
# 4. Model evaluation
Models are evaluated using Accuracy, Precision, Recall and F1 score metrics.
1. CNN model from scratch:
Test Accuracy: 14% (974/6680)
Test Precision score: 0.2170
Test Recall score: 0.1429
Test F1 score: 0.1262

2. CNN model using ResNet50 with transfer learning:
Test Accuracy: 74% (4945/6680)
Test Precision score: 0.7641
Test Recall score: 0.7221
Test F1 score: 0.7260

---
# 5. Results
Both the models, CNN from scratch and Pre-trained ResNet50 CNN with transfer learning achieved the expected test accuracies of >=10% and >=60% respectively.


