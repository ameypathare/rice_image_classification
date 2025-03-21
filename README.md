Overview Of Code:
<br>

The project involves classifying different types of rice grains using deep learning.

Dataset used: Murat Koklu's Rice Image Dataset
Loaded image dataset from local storage
Extracted image class names dynamically
Displayed sample images from each class <br>
Data Preprocessing

${\color{red}Null \space Handling \space used:}$

Checked for missing labels
Ensured all images have a valid class
${\color{red}Duplicate \space Handling \space used}$

Checked for duplicate images (if any)
${\color{red}Image \space Preprocessing}$

Rescaled images to (224, 224)
Normalized pixel values (rescale=1.0/255) <br>
Performed Exploratory Data Analysis (EDA)

Visualized sample images from each rice class
Checked class distribution <br>
Charts used

BarChart (Class Distribution)
Sample Image Grid <br>
Train-Test Split

Split data into training, validation, and test sets <br>
Model Development

Used a custom CNN model
Applied Conv2D, MaxPooling2D, BatchNormalization, Dropout
Implemented categorical cross-entropy loss function <br>
Training Process

Used ModelCheckpoint for saving the best model
Applied ReduceLROnPlateau for learning rate adjustment
Trained the model for 10 epochs <br>
Charts used for model evaluation

Accuracy vs Epochs
Loss vs Epochs
Learning Rate vs Epochs <br>
Model Evaluation

Generated classification report
Plotted confusion matrix <br>
