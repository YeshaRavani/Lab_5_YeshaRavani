# Lab_5_YeshaRavani
This repository contains the completed Jupyter Notebook, analysis, visualisations, and documentation for Lab 5 of Machine Learning and Pattern Recognition (Spring 2026).

# Aim
The objective of this lab is to explore and implement distance-based learning and clustering techniques in the context of computer vision. The task involves detecting the faces of Plaksha faculty members from a given image, extracting relevant colour-based features, and applying the K-Means clustering algorithm to group similar faces. Finally, the learned clusters are used to classify a new template image based on feature similarity.

# Methodology
1. Image Acquisition and Preprocessing
The input image was first loaded using OpenCV. Since face detection works more effectively on grayscale images, the original image (in BGR format) was converted to grayscale before further processing.
2. Face Detection
Faces were identified in the grayscale image using the Haar Cascade Classifier. This step allowed us to locate and extract the bounding boxes corresponding to each detected face.
3. Feature Extraction
Each detected face region was converted from BGR to the HSV colour space. From this representation, the mean Hue and Saturation values were calculated. These values served as compact numerical features to represent each face.
4. Clustering using K-Means
The extracted Hue–Saturation feature vectors were then clustered into two groups using the K-Means algorithm. This helped in grouping faces with similar colour characteristics.
5. Centroid Computation
For each cluster formed by K-Means, the centroid was computed. These centroids represent the central point of each cluster in the feature space.
6. Template Classification
A separate template image was processed using the same steps—face detection and feature extraction. The trained K-Means model was then used to determine which cluster the template face belongs to.
7. Visualisation
Finally, scatter plots were generated to visualise the clustering results in feature space, and bounding boxes were drawn on the original image to observe the detected faces and classification outcomes.

# Key Findings
- Faces can be effectively represented using simple colour-based features.
- The Hue and Saturation components provided clear and meaningful separation between different face regions in the feature space.
- The K-Means algorithm successfully grouped faces based on similarity in their extracted colour features.
- The template image was correctly classified into one of the learned clusters, demonstrating the effectiveness of the clustering approach.

# Conclusion
This lab demonstrated how distance-based learning and clustering techniques can be effectively applied to computer vision tasks. Even simple colour-based features, such as Hue and Saturation, were sufficient to create meaningful groupings of faces. Furthermore, these clusters could be used to classify a new template image, showing how unsupervised learning methods can support basic classification tasks. Overall, the lab highlights the importance of careful feature selection and clear visual interpretation when working with clustering and other unsupervised learning approaches.

# Visual Results
<img width="640" height="457" alt="Screenshot 2026-02-15 at 8 39 35 PM" src="https://github.com/user-attachments/assets/367a1dcd-a4eb-4a34-98fd-458db07b97c8" />
<img width="1071" height="583" alt="Screenshot 2026-02-15 at 8 40 53 PM" src="https://github.com/user-attachments/assets/b4414d41-bb48-4ed3-85f3-50e7bfac6177" />
<img width="1070" height="581" alt="Screenshot 2026-02-15 at 8 41 12 PM" src="https://github.com/user-attachments/assets/f300dd45-5a04-4af8-8130-2ddadeefe40e" />
<img width="400" height="430" alt="Screenshot 2026-02-15 at 8 41 31 PM" src="https://github.com/user-attachments/assets/dd187a43-3582-47b6-bc60-f82ec4811267" />
<img width="1067" height="581" alt="Screenshot 2026-02-15 at 8 41 46 PM" src="https://github.com/user-attachments/assets/cfa763a3-1e46-4c6a-aceb-c7581745830c" />
<img width="1068" height="583" alt="Screenshot 2026-02-15 at 8 42 07 PM" src="https://github.com/user-attachments/assets/49dc526c-0e5b-4ac7-bb2b-10102bf7c9c3" />



