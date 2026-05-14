## Google Colab link (https://colab.research.google.com/drive/1TDKTLsBWg1lqCEbkiIXkEeyfSgeqqQmr?usp=sharing)

# GUIDE QUESTIONS (Student Explanation & Reflection)

---

## A. Model Evaluation Analysis

### 1. What were the weakest-performing classes based on the confusion matrix?
-Based on the confusion matrix, Capsicum_Frutescens and Capsicum_Peppers were the weakest-performing classes. The model frequently confused these two classes because they share very similar visual characteristics such as shape, color, and texture.

### 2. How did Precision, Recall, and F1-score vary across classes?
-The performance metrics varied across classes. Some classes, such as Red_Hot_Cherry, achieved high Precision, Recall, and F1-scores (above 0.80), indicating strong classification performance. However, classes like Capsicum_Frutescens had lower scores (around 0.57), showing that the model struggled to identify their unique features consistently.

### 3. What does a low recall indicate in your model?
-A low Recall score means that the model failed to correctly identify many actual samples belonging to a class. For example, a Recall of 0.51 indicates that approximately 49% of the true samples in that class were missed or incorrectly classified.

### 4. How does AUC score reflect model performance compared to accuracy?
-The AUC score measures the model’s ability to distinguish between classes across different classification thresholds. Although the model achieved an Accuracy of 0.71, the higher AUC score of 0.92 suggests that the model is generally effective at separating classes, even if its top prediction is not always correct.

---

## B. Model Improvement

### 5. How did data augmentation affect validation accuracy?
-Data augmentation, such as image flipping and rotation, increased the diversity of training images. This prevented the model from memorizing specific samples and improved its ability to generalize, resulting in validation accuracy increasing to approximately 95%.

### 6. Why is Batch Normalization important in CNNs?
-Batch Normalization stabilizes and normalizes the values passing through neural network layers during training. This improves training speed, reduces instability, and helps the model converge more effectively.

### 7. What role did Dropout play in improving your model?
-Dropout helped reduce overfitting by randomly disabling some neurons during training. This forced the model to learn more robust and generalized patterns instead of relying on specific features or noise in the dataset.

### 8. How did Early Stopping prevent overfitting?
-Early Stopping monitored the model’s validation performance and automatically stopped training once improvements stopped occurring. This prevented the model from over-training and learning unnecessary noise from the training data.
---

## C. Performance Comparison

### 9.After improving the model architecture and training process, the classification accuracy increased significantly from 71% to 95%. Additionally, the loss curves became smoother and more stable, indicating better learning performance.

### 10. Which enhancement contributed the most to performance improvement? Why?
-The combination of deeper CNN layers (increasing filters from 32 to 128) and Data Augmentation contributed the most to the improvement. The deeper layers captured more complex image features, while augmentation provided more varied training samples that improved generalization.

### 11. Did the gap between training and validation accuracy decrease? Explain.
-Yes, the gap between training and validation accuracy became smaller. In some cases, validation accuracy was even slightly higher than training accuracy, which suggests that the model generalized well and avoided overfitting.

---

## D. Explainability (Grad-CAM Integration)

### 12. How did Grad-CAM help in understanding model predictions?
-Grad-CAM generated heatmaps that highlighted the regions of the image the model focused on before making predictions. This made it easier to understand how the model interpreted the pepper images.

### 13. Did the improved model focus on more relevant regions? Provide evidence.
-Yes, the Grad-CAM heatmaps were concentrated mainly on the actual pepper fruits instead of the background. This indicates that the improved model learned to focus on the most relevant image regions for classification.

### 14. Why is explainability important in real-world AI applications?
-Explainability is important because it increases trust and transparency in AI systems. In real-world applications, users and developers need to understand whether the model is making decisions based on meaningful patterns rather than irrelevant features or random correlations.
