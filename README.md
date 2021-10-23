# MinibatchKmeans-vs-Kmeans
In this notebook, I compared two famous clustering algorithm, the minibatchkmeans and the regular kmeans on image dataset.

## The data
First of all, we need to download the image data used in this comparison.

For the smal dataset:
https://drive.google.com/drive/folders/1YHGUbFLp_5HiRISBzRo3GmnM4OQpAO0T?usp=sharing

For the big dataset:
https://drive.google.com/drive/folders/1YHGUbFLp_5HiRISBzRo3GmnM4OQpAO0T?usp=sharing


The data is constitued of 4 types of white cells.
<img width="980" alt="Capture d’écran 2021-10-23 à 3 56 47 PM" src="https://user-images.githubusercontent.com/55285736/138559491-8cc0e5ad-3006-447d-b967-35fdf47e219f.png">

# The comparison

Because minibatch-kmeans aims to reduce memory constraint and decrease the cpu time, we'll compare both of the clustering algorithms on time execution.
We'll also investigate the effect of minibatch-kmans parameters such as **batch size** and eventually the **number of clusters**.
<img width="1065" alt="Capture d’écran 2021-10-23 à 3 59 25 PM" src="https://user-images.githubusercontent.com/55285736/138559608-fc8f1c00-86b6-4243-ba7c-c50a831d9814.png">

Because silhouette score weren't good, we wanted to visualize the data in a factorial plane using Linear Discriminative Analysis. Because we had the label of each class, we applied the discriminative algorithm to have less dimension to deal with, and to investigate the impact of the input space on both Kmeans and MiniBatchKmeans.
<img width="1001" alt="Capture d’écran 2021-10-23 à 4 01 32 PM" src="https://user-images.githubusercontent.com/55285736/138559715-5542d170-6a0c-4252-847f-65584e5b8865.png">

Finally, we compare both algorithms based on the silhouette score and investigate the performance.
<img width="920" alt="Capture d’écran 2021-10-23 à 4 02 54 PM" src="https://user-images.githubusercontent.com/55285736/138559757-02337036-4cd4-49c6-8cb5-c857c0f0d248.png">

We ended up with approximately the same results, and we can say  with confidence, that minibatch-kmeans is appropriate for both small and big dataset, especially with images, where It performs > 50 times faster than Kmeans.
<img width="1027" alt="Capture d’écran 2021-10-23 à 4 04 33 PM" src="https://user-images.githubusercontent.com/55285736/138559820-afb0994f-202f-4501-bba5-a169e27fe1ca.png">

