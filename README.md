# AlcoGaurd


**AlcoGuard: Detecting Drunkenness Using Accelerometer Data**

## 📌 Project Overview
AlcoGuard is a **project designed to detect drunkenness** using **smartphone accelerometer data**. The idea was to analyze motion patterns and classify whether a person is **drunk or sober** using **deep learning techniques**.

The project focused on **designing the model, preprocessing strategies, deployment plan, and security framework**, making it a **solid foundation** for a real-world application.

## 🛠 Technologies Used
- **Languages:** Python, HTML/CSS, JavaScript  
- **Libraries & Frameworks:** TensorFlow, Keras, Flask, NumPy, Pandas, Matplotlib, Scikit-Learn  
- **Tools:** Azure ML Studio, Azure Virtual Machine, Google Colab, Jupyter Notebook, POCO F1 Smartphone  

## 📖 Problem Statement
- Drunkenness **impairs motor skills and judgment**, increasing accident risks.
- Breathalyzers and blood tests are **invasive** and **not always accessible**.
- Our goal was to build a **non-invasive solution** using **accelerometer data** to detect if someone is **drunk**.

## 📊 Dataset
We used the **UCI "Bar Crawl: Detecting Heavy Drinking" dataset**, containing accelerometer readings.

| Feature | Description |
|---------|-------------|
| `x` | Acceleration along X-axis |
| `y` | Acceleration along Y-axis |
| `z` | Acceleration along Z-axis |
| `label` | 1 = Drunk, 0 = Sober |

### **Data Preprocessing**
- **Cleaning:** Removed missing/inconsistent values.
- **Normalization:** Feature scaling applied.
- **Labeling:** Mapped TAC readings to Drunk/Sober.
- **Splitting:** 70% training, 30% testing.
- **Resizing:** Data formatted for CNN input.

## 🧠 Model Design
We designed a **Convolutional Neural Network (CNN)** for classification.

### **Planned CNN Architecture**
1. **Conv2D Layer 1** - Extracts features from (80, 3, 1) input.
2. **Conv2D Layer 2** - Learns deeper patterns.
3. **Dropout Layer** - Reduces overfitting.
4. **Flatten Layer** - Converts feature maps into a vector.
5. **Dense Layer 1** - Fully connected, 128 neurons.
6. **Dropout Layer 2** - Further prevents overfitting.
7. **Dense Output Layer** - Final classification (Drunk vs. Sober).

### **Expected Model Performance**
- **Training Accuracy:** ~91.73%
- **Validation Accuracy:** ~89%

## ☁️ Cloud Deployment (Planned)
For real-time predictions, we considered deploying on **Azure Cloud**:

- **Flask API** - Processes HTTP requests.
- **Azure Virtual Machines** - Hosts the model.
- **Database** - Stores motion data for real-time analysis.

### **Proposed Workflow**
1. Smartphone collects **accelerometer data**.
2. Data is **sent to the cloud API**.
3. Model predicts if the user is **drunk or sober** and sends an **alert**.

## 🔒 Security & Compliance Considerations
- **ISO 27001** - Info security management.
- **ISO 28001** - Supply chain security.
- **CCPA & CPRA** - California privacy laws.
- **PDPA** - Personal data protection.
- **GDPR** - EU data protection.
- **FedRAMP** - Secure cloud computing.

### **Privacy Measures**
- No **location tracking** to avoid ethical issues.
- Strict **data protection** rules applied.

## 🚧 Challenges Faced
1. **Privacy Concerns** - Initial geolocation tracking was **removed** to comply with privacy laws.
2. **Cloud Deployment Issues** - Faced **TensorFlow & Azure conflicts**, suggested **Dockerization**.
3. **Model Limitation** - It **only detects drunkenness**, does not predict future behavior.


## 🚀 Future Scope
🔹 Implement **real-time mobile inference**.  
🔹 Improve model to **predict drunken behavior** before it happens.  
🔹 Optimize CNN for **higher accuracy & efficiency**.  
🔹 Conduct **real-world tests** to validate the model.

