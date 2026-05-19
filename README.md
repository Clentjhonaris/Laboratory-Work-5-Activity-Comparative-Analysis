# Laboratory-Work-5-Activity-Comparative-Analysis

https://colab.research.google.com/drive/1yndSC9otAt-Chi92Jl79qHXWpWbXm7E8?usp=sharing

| Model / Sample                         | Train Accuracy | Train Loss | Test Accuracy | Test Loss | Precision | Recall | F1-score | ROC AUC |
|----------------------------------------|----------------|------------|---------------|-----------|-----------|--------|----------|---------|
| Pre-Trained Model 1 (EfficientNetB0)   | 0.8521         | 0.4120     | 0.0420        | 2.8540    | 0.0120    | 0.0420 | 0.0105   | 0.5012  |
| Pre-Trained Model 2 (ResNet50)         | 0.3618         | 2.1763     | 0.5045        | 1.9095    | 0.2589    | 0.2711 | 0.2486   | 0.7614  |
| Pre-Trained Model 3 (MobileNetV2)      | 0.6366         | 1.3724     | 0.7321        | 1.2329    | 0.7325    | 0.7281 | 0.7254   | 0.9515  |
| Model from Teachable Machine           |0.9859          | 0.0052     | 0.9750        |  0.1910   | 0.0000    | 0.0000 | 0.0000   | 0.0000  |
| Your 1st Model                         | 0.9520         | 0.0828     | 0.6080        | 1.9856    | 0.6232    | 0.6080 | 0.6056   |  0.9423 |
| Your 2nd Model Enhancement             | 0.7985         | 1.6977     | 0.7450        | 0.9295    | 0.7598    | 0.7450 | 0.7467   | 0.9051  |
|  Your 3rd Model – The Good Model       | 0.3306         | 2.3665     | 0.4615        | 2.1846    | —         | —      | —        |   —     |  


## 🧠 GUIDE QUESTIONS (FINAL REFLECTION)

### A. Model Performance
- **Best Performing Model:** MobileNetV2 model achieved the highest performance among the pre-trained models
- **Lowest Performance:** EfficientNetB0 model had the lowest performance.
- **Generalization Gap:**  The loss values show clear differences in how well each model learned.

  ---

### B. Evaluation Metrics
- **Why Accuracy is Not Enough:** Accuracy alone is not enough to evaluate model performance because it only measures the total number of correct predictions without considering how errors are distributed across classes. 
- **Best F1-score:** The best F1-score was achieved by the MobileNetV2 model, with a value of 0.7254.
- **Observation:** The Teachable Machine model shows very high accuracy but lacks meaningful classification metrics (precision, recall, F1, ROC AUC = 0), which suggests that its evaluation is incomplete or not properly computed.

  ---

### C. Confusion Matrix Insights
-  **Frequent Errors:** The most frequent errors occur when the models confuse visually similar classes. This is especially noticeable in the weaker models such as EfficientNetB0 and ResNet50, where predictions often fall into incorrect but closely related categories. These misclassifications suggest that the models struggle to extract highly discriminative features for certain classes in the dataset.
- - **Pattern:** This indicates that better-performing models are more effective at learning class-specific features, while weaker models rely more on general patterns and fail to separate similar categories properly

---
### D. ROC Curve & AUC
- **Top AUC Score:** The highest ROC AUC score was achieved by the MobileNetV2 model, with a value of 0.9515
- **Meaning:** The ROC AUC score measures how well a model can distinguish between different classes. A higher value (closer to 1.0) means the model has a strong ability to correctly separate classes and make confident predictions.


  ---

### E. Explainability (Grad-CAM)
- **Findings:** MobileNetV2 focuses more on the correct object areas in the image, while weaker models sometimes focus on background or irrelevant regions.
-  **Insight:** Better models like MobileNetV2 have clearer attention maps, meaning they learn important features more effectively, while weaker models show less focused and more scattered attention.



---

### F. Model Improvement
- **Recommended Model:** The recommended model is MobileNetV2 because it has the best overall balance of accuracy, F1-score, and ROC AUC, making it the most reliable for classification and real-world use.
- **Ways to Improve:** Train for more epochs
Use data augmentation
Fine-tune more layers
Tune learning rate and batch size
Apply class balancing
Use early stopping / learning rate scheduling


---

### G. Real-World Application
- **Use Case:** The model can be used for image classification tasks such as object recognition in mobile apps, automated sorting systems, or educational tools.
- **Risk:** Possible risks include misclassification of similar objects, reduced accuracy on new/unseen data, and bias if the dataset is not balanced.
- **Deployment:** The model can be deployed using mobile or web applications through TensorFlow Lite or cloud-based APIs, allowing real-time image prediction with lightweight performance.

---

  
