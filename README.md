# ml-lulc-hc-opt
Estimation of land cover classification using Hierarchical clustering approach with optical satellite

Hierarchical clustering is a common technique used in unsupervised learning. Because hierarchical clustering is a process that requires considerable machine power, we recommend using GPUs to process the data. Therefore, this chapter assumes that the analysis is performed using Google Colab and also narrows the scope of the analysis.

The following flow of explanation is provided.

- What is hierarchical clustering?
- Mathematical background of hierarchical clustering
- Apply the approach

Approach is below:
- Step1: Import library
- Step2: Search scene and extract required data
- Step3: Extract feature
- Step4: Classification
- Step5: Get clusters with a specified number of clusters
- Step6: Visualization of Classification Results
- Step7: Evaluation of the accuracy of classification

## Classification
Classification by hierarchical clustering using the features. This time, we will classify the data into 5 classes. This time we will use the cluster module of scipy. Please refer to the official documentation for details.

[dedrogram]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/c71f68bb-8753-4a22-ac79-090819d1b6dc)

[Visualization]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/0debefd0-07f4-48c2-923d-237dd0b54691)

## Validation
The accuracy of the classification results is evaluated. The evaluation of classification accuracy is usually expressed using a confusion matrix (also called a classification accuracy matrix or classification efficiency table). This is a tabular representation of the results of a classification problem, with the "actual class" and "predicted class" as axes.
The validation data is rearranged into the following classification classes
0: Unclassified
1: Water → Water body
2: Urban → Artificial
3: Rice paddy → Grassland/farmland
4: Crops → Grassland
5: Grassland → Grassland/farmland
6: Deciduous broadleaf tree (DBF) → Forest
7: Deciduous coniferous (DNF) → Forest
8: Evergreen broadleaf tree (EBF) → Forest
9: Evergreen coniferous (ENF) → Forest
10: Bare land → Grassland/farmland
11: Bamboo forest (Bamboo) → Forest
12: Solar panel → Artificial

[LC_N42E144.tif]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/7b53b139-6a2d-495a-858b-02c2e0a6973c)

[LC_N43E144.tif]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/7ead089e-f691-44e7-8df6-34949ca7ed4d)


[val_im.tif]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/46615d02-ba7c-4078-92bc-bb108baf998c)

[cut_val_im.tif]

![image](https://github.com/jutak0228/ml-lulc-hc-opt/assets/159540763/c2ac1afe-4120-4fd8-9e1b-e753a8061f6a)
