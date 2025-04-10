# AI-MODEL-SMART-CATTLE-HEALTH-MONITORING
Introducing an AI model built using STM32BL475EIOT1A board and deep learning to revolutionize the monitoring process. dairy cows' health and well-being are paramount.
 To address this issue, In this project machine-learning model that can detect the health condition of cattle based on various parameters like body temperature, pulse rate, respiratory rate, rumen fill, etc![image](https://github.com/user-attachments/assets/a4c15b31-7aa3-4dcc-bb8f-b51fc848ff27)
Neural Network Architecture:
Input Layer (Dense):   Size: 64 neurons Activation Function: Rectified Linear Unit (ReLU) 
Hidden Layer (Dense): Size: 32 neurons Activation Function: Rectified Linear Unit (ReLU) 
Output Layer (Dense): Size: Dependent on the number of classes in the target variable Activation Function:
Softmax (for multi-class classification using sparse categorical cross-entropy).
Model Training
Split Dataset: Divide the dataset into training and validation sets (80% training, 20% validation). • 
Training: Train the model for 150 epochs with a batch size of 10 using the numerical features as input and the target variable (health status) for supervision. 
 Model Evaluation: Evaluate the model on the validation set to assess its performance in terms of loss and accuracy. 
. Prediction and Evaluation • Generate predictions on the validation set and convert them to binary format based on a threshold of 0.5
• Generation of the C code for the model The model can feed to STM32 MX Tool. In that tool, we select a board after that we can feed the model and select the analysis and validation and it can generate c code for this model.
• Validation on target Set up an STM32 project in Cube IDE, select the microcontroller variant, and configure settings. Add ML libraries, integrate the model code, prepare input data, run inference, and validate results in Cube IDE
