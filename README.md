${\color{red}Overview \space of \space code}$  
- **The project is executed in a local environment using TensorFlow and Keras for deep learning.**  
  - **Dataset Source:** Kaggle – *Rice Image Dataset*  
  - **Data Organization:**  
    - Images are organized into folders based on class labels.  
  - **Process Overview:**  
    - Data is loaded, preprocessed, and trained using a custom CNN model.  

---

${\color{red}Data \space Preparation}$  

- **Loaded image files from local directories.**  
- **Created a DataFrame containing image paths and labels.**  
- **Shuffled data to ensure randomness in training.**  

---

${\color{red}Data \space Cleaning}$   

### **Null Handling used:**  
- `isnull()`  
- `notnull()`  
- `dropna()`  
- `fillna(value)`

### **Duplicate Handling used:**  
- `drop_duplicates()`  

---

${\color{red}Data \space Preprocessing}$   

- **Rescaled image pixel values** using `ImageDataGenerator`.  
- **Defined image size:** *(224x224)*.  
- **Used batch processing** with `batch_size=16`.  

---

${\color{red}EDA}$   

- **Displayed sample images from each class.**  
- **Plotted image count distribution per class.**  

---

${\color{red}Visualization}$    

- **Bar Chart** – Visualized class distribution.  
- **Box Plot** – Analyzed pixel intensity variations.  
- **Pairplot** – Checked image feature relationships.  
- **Heatmap** – Displayed confusion matrix for model evaluation.  

---

${\color{red}Modelling}$   

### **Custom CNN Model**  
- **Input shape:** `(224, 224, 3)`  
- **Layers Used:**  
  - `Conv2D` and `MaxPooling2D` for feature extraction.  
  - `BatchNormalization` to stabilize learning.  
  - `Dropout` to prevent overfitting.  
- **Output layer:** Uses `Softmax` activation for multi-class classification.  

---

## *Model Training*  

- **Loss function:** `CategoricalCrossentropy`  
- **Optimizer:** `Adadelta` with `learning_rate=0.01`  
- **Training Enhancements:**  
  - `ModelCheckpoint` – Saves the best model.  
  - `ReduceLROnPlateau` – Adjusts learning rate dynamically.  

---

## *Performance Evaluation*  

- **Accuracy Plot** – Compared training and validation accuracy.  
- **Loss Plot** – Visualized loss trends over epochs.  
- **Learning Rate Plot** – Monitored changes in learning rate.  

---

## *Testing & Predictions*  

- **Generated predictions on test data.**  
- **Created a classification report** with *precision, recall, and F1-score*.  
- **Displayed sample test images** with predicted labels and confidence scores.  

---

## *Model Evaluation*  

- **Confusion Matrix** – Analyzed classification performance.  
- **Identified misclassified images** to assess model weaknesses.  

---

## *Final Outcome*  

- **Successfully classified different rice types with high accuracy.**  
- **Improved model generalization** using *data augmentation and regularization techniques.*  
