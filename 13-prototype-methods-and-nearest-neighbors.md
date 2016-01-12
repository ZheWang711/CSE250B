# Prototype Methods and Nearest-Neighbors

## 13.2 Prototype Methods
The main challenge is to figure out how many prototypes to use and where to put them. Methods differ according to the number and way in which prototypes are selected.

### 13.2.1 K-means Clustering
1. Unlabeled data
2. Labeled data
    * Apply K-means clustering to the training data in each class separately, using R prototypes per class;
    * Assign a class label to each of the K $$\times$$ R prototypes;
    * Classify a new feature x to the class of the closest prototype.

### 13.2.2 LVQ algorithm
