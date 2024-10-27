### **Introduction**

This repository contains a fully connected feedforward neural network created with Keras, designed for binary classification of heart disease. The model is trained on a dataset consisting of various patient attributes, including medical history, lifestyle factors, and demographics.

### **Dataset**

The dataset used for training and evaluation is provided in directory. It includes the following columns:

* **HeartDiseaseorAttack:** Target variable indicating whether a person has experienced a heart disease or attack (0 or 1).
* **HighBP:** Indicates whether the person has high blood pressure.
* **HighChol:** Indicates whether the person has high cholesterol.
* **CholCheck:** Indicates whether the person has had a cholesterol check.
* **BMI:** Body Mass Index.
* **Smoker:** Indicates whether the person is a smoker.
* **Stroke:** Indicates whether the person has had a stroke.
* **Diabetes:** Indicates whether the person has diabetes.
* **PhysActivity:** Indicates whether the person is physically active.
* **Fruits:** Indicates how often the person eats fruits.
* **Veggies:** Indicates how often the person eats vegetables.
* **HvyAlcoholConsump:** Indicates whether the person consumes heavy alcohol.
* **AnyHealthcare:** Indicates whether the person has any healthcare coverage.
* **NoDocbcCost:** Indicates whether the person has no doctor because of cost.
* **GenHlth:** General health rating.
* **MentHlth:** Mental health rating.
* **PhysHlth:** Physical health rating.
* **DiffWalk:** Indicates whether the person has difficulty walking.
* **Sex:** Gender.
* **Age:** Age.
* **Education:** Education level.
* **Income:** Income level.

---

### Model Architecture

1. **Input Layer**: The input layer expects data of shape `(21,)`, where 21 is the number of input features.

2. **Hidden Layers**:
   - **Dense Layer 1**: A fully connected layer with 128 units, using a Sigmoid activation function and HeNormal initialization for the kernel weights.
   - **Dense Layer 2**: A fully connected layer with 64 units, also using a Sigmoid activation and HeNormal kernel initialization.
   - **Dense Layer 3**: A fully connected layer with 32 units, with Sigmoid activation and HeNormal kernel initialization.

3. **Output Layer**:
   - **Dense Layer**: A single-unit fully connected layer with Sigmoid activation, producing the probability for the binary classification task.

4. **Loss Function**: Binary Crossentropy is used as the loss function, appropriate for binary classification.

5. **Optimizer**: Adam optimizer is used with a learning rate of 0.001 and gradient clipping (`clipvalue=1.0`) to prevent gradient explosion.

**Training Setup**: The model is trained over 30 epochs, with mini-batches of size 32. Accuracy is used as the evaluation metric to monitor performance.


### **Usage**

1. **Install dependencies:** Ensure you have the necessary libraries installed, including TensorFlow, Keras, and NumPy.
2. **Prepare data:** Load the dataset and preprocess it as needed (e.g., handle missing values, normalize features).
3. **Train the model:** Run the training script to train the model on the prepared dataset.
4. **Evaluate performance:** Evaluate the model's performance using appropriate metrics such as accuracy, precision, recall, F1-score, and AUC-ROC.

