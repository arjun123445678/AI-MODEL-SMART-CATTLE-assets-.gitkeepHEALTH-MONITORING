# 🐄 AI-MODEL-SMART-CATTLE-HEALTH-MONITORING

An AI-powered smart cattle health monitoring system developed using the **STM32 B-L475E-IOT01A** board. This project leverages **deep learning** and embedded **Edge AI** to monitor the health status of dairy cows in real-time, helping to improve animal welfare and prevent potential diseases.

---

## 📌 Project Overview

This system uses a trained neural network model optimized for deployment on STM32 microcontrollers. Sensor data such as temperature, humidity,  are used to classify cattle health into categories like **Normal**, **Mild**, or **Severe** stress.

---

## 🧠 AI Model Architecture

- **Input Layer**:  
  - Type: Dense  
  - Size: 64 neurons  
  - Activation: ReLU

- **Hidden Layer**:  
  - Type: Dense  
  - Size: 32 neurons  
  - Activation: ReLU

- **Output Layer**:  
  - Type: Dense  
  - Size: Depends on number of classes  
  - Activation: Softmax (for multi-class classification)

---

## 📊 Model Training

- **Dataset Split**:  
  - 80% Training  
  - 20% Validation

- **Training Parameters**:  
  - Epochs: 150  
  - Batch Size: 10  
  - Loss Function: Sparse Categorical Crossentropy  
  - Optimizer: Adam

- **Evaluation**:  
  - Performance evaluated on the validation set using accuracy and loss metrics.  
  - Predictions converted to binary format using a threshold of 0.5.

---

## ⚙️ Model Deployment on STM32

### 1. Generate C Code
- Use **STM32Cube.AI** (integrated in STM32CubeMX) to:
  - Import the `.h5` model
  - Run analysis and validation
  - Generate C code for inference

### 2. Setup STM32CubeIDE Project
- Select **STM32 B-L475E-IOT01A**
- Add Cube.AI and X-CUBE-AI middleware
- Integrate the generated model files into the project
- Prepare input sensor data (temperature, humidity, activity)
- Run inference and display results (e.g., on UART or LCD)

---

## 🔌 Hardware Requirements

- STM32 B-L475E-IOT01A board  

---

## 🖥️ Software Requirements

- STM32CubeIDE  
- STM32CubeMX  
- Python (for model training, optional)  
- TensorFlow / Keras  
- STM32Cube.AI Toolkit

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## 🤝 Acknowledgements

- STMicroelectronics for the STM32 ecosystem  
- TensorFlow/Keras for model building  
- Community contributors for tutorials and support

---

## 🚀 Future Work

- Cloud dashboard integration using ESP8266 + ThingSpeak  
- Add real-time alert system (SMS/Push Notification)  
- Expand model with time-series data for improved accuracy


## 💬 Contact

For questions or collaboration, feel free to reach out via GitHub Issues or email.

