# Online-Payments-Fraud-Detection-Using-Machine-Learning
🛡️ Project Overview: Online Payments Fraud Detection
📌 1. Introduction
With the surge in digital transactions, the risk of fraudulent activities has escalated. This project implements an automated, machine learning-based system designed to identify suspicious patterns and prevent financial fraud in real-time, restoring user trust in digital payment ecosystems.

🎯 2. Project Objectives
Accuracy: Detect fraudulent transactions with high precision.

Security: Build a reliable system to minimize financial losses.

User Experience: Develop a user-friendly web interface for real-time predictions.

Automation: Replace manual monitoring with efficient automated analysis.

🧠 3. Problem Statement
Traditional fraud detection methods are often manual, time-consuming, and prone to error. As transaction volumes grow, these methods fail to scale, creating a need for an automated system capable of processing large datasets and delivering instant results.

📊 4. Dataset Description
The model is trained on transaction logs containing the following key features:

step: Unit of time (1 step = 1 hour).

type: Type of transaction (CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).

amount: The transaction value.

oldbalanceOrg: Sender’s balance before the transaction.

newbalanceOrig: Sender’s balance after the transaction.

oldbalanceDest: Receiver’s balance before the transaction.

newbalanceDest: Receiver’s balance after the transaction.

isFraud: Target variable (0 = Legitimate, 1 = Fraud).

⚙️ 5. Technical Implementation
System Architecture
The application follows a streamlined pipeline:
User Input → Web Interface (Frontend) → Flask API (Backend) → ML Model → Result Output

Data Preprocessing
Cleaning: Removed redundant or unnecessary columns.

Encoding: Converted categorical data (like transaction types) into numeric formats.

Imputation: Handled missing values to ensure data integrity.

Splitting: Divided data into an 80% Training set and 20% Testing set.

Machine Learning Model
After testing multiple algorithms (Decision Tree, SVM), the Random Forest Classifier was selected as the final model.

Why Random Forest? It offers superior accuracy, manages large datasets efficiently, and reduces the risk of overfitting through ensemble learning.

🌐 6. Web Application & Interface
The system is deployed as a web application using the following stack:

Frontend: HTML and CSS for a responsive, interactive UI.

Backend: Flask (Python) to bridge the user interface and the ML model.

Model Persistence: The trained model is saved as fraud_model.pkl using joblib for rapid loading.

Core Pages:

Home: Introduction and overview.

Prediction: Form for entering transaction details.

Result: Real-time display of "Fraud" or "Not Fraud" status.

📈 7. Performance & Evaluation
The system was validated using several metrics to ensure reliability:

Accuracy: Overall correctness of the model.

Precision & Recall: Measuring the model's ability to catch true fraud without excessive false alarms.

Testing:

Case 1: Small amount (e.g., 500) → Result: Not Fraud.

Case 2: High-risk pattern (e.g., 100,000) → Result: Fraud.

🚀 8. Future Scope & Limitations
Limitations:

Dependent on the quality and diversity of the training dataset.

Potential for false positives in edge cases.

The Road Ahead:

Integrating directly with live banking APIs.

Implementing Deep Learning models for complex pattern recognition.

Developing a dedicated mobile application.

🏁 9. Conclusion
This project successfully demonstrates how machine learning can be leveraged to secure digital payments. By combining a Random Forest backend with a Flask web interface, the system provides an accessible and effective tool for real-time fraud prevention.
