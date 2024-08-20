## Credit Card Fraud Detection

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The notebook guides through the steps of data preprocessing, handling class imbalance, and implementing a neural network model for accurate fraud detection.

### Project Overview:
1. **Exploratory Data Analysis (EDA):**
   - Performs detailed EDA processes to understand the structure of the data, identify any duplicate entries, and check for missing values.

2. **Handling Class Imbalance:**
   - **Synthetic Minority Over-sampling Technique (SMOTE):** The dataset is highly imbalanced, with far fewer fraudulent transactions than non-fraudulent ones. SMOTE is used to create synthetic samples for the minority class, ensuring balanced classes in the training set.

3. **Data Normalization:**
   - The 'Amount' column is standardized using `StandardScaler` to ensure that the feature values are on the same scale, which improves the performance of the neural network.

4. **Neural Network Implementation:**
   - **Model Architecture:**
     1. A neural network model (SimpleNN) with three fully connected layers.
     2. The input layer consists of 30 features derived from the 'Time' and 'Amount' columns and 28 PCA components.
     3. Two hidden layers use ReLU activation functions with 16 and 8 neurons, respectively.
     4. The output layer has a single neuron with a sigmoid activation function, providing the probability for binary classification.
   - **Training Process:**
     - The model is trained using the binary cross-entropy loss function and the Adam optimizer over 20 epochs.
     - Both training and validation loss and accuracy are tracked to monitor model performance.

5. **Model Evaluation:**
   - **Training Loss and Accuracy:**
     - The training loss steadily decreases over the epochs, indicating that the model is effectively learning from the data.
     - The training accuracy improves, showing that the model is becoming proficient at correctly classifying the training instances.
   - **Validation Loss and Accuracy:**
     - The validation loss also decreases, suggesting that the model is generalizing well to unseen data.
     - The validation accuracy improves, highlighting the model's ability to correctly identify fraudulent transactions.

6. **Results:**
   - The model shows high accuracy in both training and validation phases, indicating robust performance in identifying credit card fraud.
   - The final accuracy metrics reflect the model's capacity to generalize well to new, unseen data.

### How to Use:
1. **Clone the Repository:**
   - Clone the repository to your local machine using `git clone`.
   
2. **Install Dependencies:**
   - Install the required Python libraries listed in the `requirements.txt` file using `pip install -r requirements.txt`.

3. **Run the Notebook:**
   - Open the notebook in Jupyter and execute the cells sequentially to perform the analysis and train the models.

### Conclusion:
This project demonstrates a complete pipeline for detecting credit card fraud using a neural network model. It includes essential steps like handling data imbalance, normalizing features, and implementing a robust model for accurate classification of fraudulent transactions.
