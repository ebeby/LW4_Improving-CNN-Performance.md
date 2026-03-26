## Google Colab link (https://colab.research.google.com/drive/1TDKTLsBWg1lqCEbkiIXkEeyfSgeqqQmr?usp=sharing)

# GUIDE QUESTIONS (Student Explanation & Reflection)

---

## A. Model Evaluation Analysis

### 1. What were the weakest-performing classes based on the confusion matrix?
-Based on the confusion matrix, Capsicum_Frutescens and Capsicum_Peppers were the weakest. They were often confused with each other because they look very similar.

### 2. How did Precision, Recall, and F1-score vary across classes?
-Performance wasn't the same for all. Red_Hot_Cherry had high scores (over 0.80), but Capsicum_Frutescens was low (0.57), showing the model struggled with its specific features.

### 3. What does a low recall indicate in your model?
-A low recall (0.51) means the model missed 49% of the actual peppers in that class. It simply didn't recognize them as the correct type.

### 4. How does AUC score reflect model performance compared to accuracy?
-My AUC (0.92) was much higher than my Accuracy (0.71). This means the model is actually good at distinguishing classes, even if it doesn't always pick the right one as its first choice.

---

## B. Model Improvement

### 5. How did data augmentation affect validation accuracy?
-Adding flips and rotations stopped the model from "memorizing" images. This helped the validation accuracy jump to ~95%.

### 6. Why is Batch Normalization important in CNNs?
-This kept the math stable inside the layers. it made the training faster and more reliable.

### 7. What role did Dropout play in improving your model?
-I used Dropout to randomly "turn off" parts of the brain during training. This forced the model to learn better patterns instead of relying on "lucky" pixels.

### 8. How did Early Stopping prevent overfitting?
-This tool stopped the training automatically once the model stopped improving. it prevented the model from over-training and "learning the noise."

---

## C. Performance Comparison

### 9. What improvements were observed after modifying the model?
-The biggest change was the accuracy jump from 71% to 95%. The loss graphs also showed a much smoother downward trend.

### 10. Which enhancement contributed the most to performance improvement? Why?
-The deeper CNN layers (32 to 128 filters) combined with Data Augmentation worked best. More layers captured more detail, and augmentation provided more variety.

### 11. Did the gap between training and validation accuracy decrease? Explain.
-The gap between training and validation was small. Since Validation was actually higher than Training at times, it proves the model is generalized and not just memorizing data.

---

## D. Explainability (Grad-CAM Integration)

### 12. How did Grad-CAM help in understanding model predictions?
-Grad-CAM showed me a "heatmap" of the image. It let me see exactly where the model was looking before it made a guess.

### 13. Did the improved model focus on more relevant regions? Provide evidence.
-The heatmaps were centered on the actual pepper fruit. This proves the model was looking at the right thing, not the background.

### 14. Why is explainability important in real-world AI applications?
-Explainability is about trust. In the real world, we need to know the AI is making decisions for the right reasons, not just by accident.
