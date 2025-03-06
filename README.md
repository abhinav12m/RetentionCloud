---

### **🚀 RetentionCloud 🤖**
**Predict Customer Lifetime Value & Churn using Machine Learning & AWS!**

---

## **🧠 Why This Project?**
Ever wondered how banks and businesses know **which customers to retain** and **which ones are at risk of leaving**? 

This project **solves that mystery** using **Machine Learning** & **AWS**! We predict:
- **💰 Customer Lifetime Value (CLV)** → How much revenue a customer will generate.
- **⚠️ Customer Churn** → Whether a customer is likely to leave.

✨ What makes this project special?
- **End-to-end AWS ML deployment**: Train locally, deploy globally! 🌍
- **Real-time predictions using AWS Lambda & API Gateway** ⚡
- **Fully scalable infrastructure using AWS SageMaker & S3** ☁️
- **Interactive Streamlit UI for easy access** 🎨

---

## **🛠️ Tech Stack & Tools**
This project combines **Machine Learning** with **Cloud Deployment** 🚀.

| **Category**        | **Tech Used** |
|---------------------|--------------|
| **Machine Learning** | Python, Scikit-Learn, XGBoost, SMOTE |
| **Data Processing** | Pandas, NumPy, Matplotlib, Seaborn |
| **Cloud Deployment** | AWS S3, AWS Lambda, AWS SageMaker, AWS API Gateway |
| **Infrastructure** | Boto3, AWS CLI, IAM Roles |
| **Frontend** | Streamlit (for interactive UI) |
| **Version Control** | Git, GitHub |

---

## **📂 Project Structure**
```
CLV&CHURN/
│── models/                    # Saved ML models
│   ├── clv_model.pkl
│   ├── churn_model.pkl
│── scripts/                    # All automation scripts
│   ├── prepare_models.py        # Convert .pkl models to .tar.gz
│   ├── upload_models.py         # Upload models to S3
│   ├── deploy_sagemaker.py      # Deploy models on AWS SageMaker
│   ├── lambda_function.py       # AWS Lambda function for inference
│   ├── streamlit_app.py         # Streamlit frontend
│── requirements.txt             # Python dependencies
│── README.md                    # You’re reading this! 😎
```

---

## **🚀 Getting Started**
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/CLV-CHURN-Prediction.git
cd CLV-CHURN-Prediction
```

### **2️⃣ Set Up AWS Credentials**
Make sure you have **AWS CLI installed** and configured:
```bash
aws configure
```
Enter:
- **AWS Access Key ID**
- **AWS Secret Access Key**
- **Region Name** (e.g., `us-east-1`)
- **Output format**: `json`

### **3️⃣ Set Up Virtual Environment**
```bash
python3 -m venv venv
source venv/bin/activate  # (For Mac/Linux)
venv\Scripts\activate      # (For Windows)
pip install -r requirements.txt
```

---

## **🎯 Step-by-Step Workflow**
### **🔹 1. Convert `.pkl` Models to `.tar.gz` for AWS**
```bash
python scripts/prepare_models.py
```
✅ This ensures that models are **AWS-compatible**.

### **🔹 2. Upload Models to S3**
```bash
python scripts/upload_models.py
```
✅ Models are now **securely stored in AWS S3**.

### **🔹 3. Deploy Models to AWS SageMaker**
```bash
python scripts/deploy_sagemaker.py
```
✅ This **hosts the models as SageMaker Endpoints**.

### **🔹 4. Deploy AWS Lambda for Real-Time Predictions**
1. Go to **AWS Lambda Console** → **Create Function** → **Python 3.10**.
2. Copy & paste `scripts/lambda_function.py`.
3. Deploy it and **link it to API Gateway**.

### **🔹 5. Set Up API Gateway**
1. Go to **AWS API Gateway** → **Create REST API**.
2. Link to **Lambda Function**.
3. Deploy and **copy the Invoke URL**.

---

## **🖥️ Running the Streamlit Frontend**
Once API Gateway is deployed, run:
```bash
streamlit run scripts/streamlit_app.py
```
🌟 **Open the UI in your browser** and test predictions!

---

## **📌 Troubleshooting & FAQs**
❓ **Q: I get a `NoSuchBucket` error when uploading models.**  
👉 Run `aws s3 ls` to check if the bucket exists. If not, create it manually:
```bash
aws s3 mb s3://bank-churn-models
```

❓ **Q: I get an `AccessDenied` error when creating IAM roles.**  
👉 Ask your AWS admin to **grant IAMFullAccess permissions** to your user.

❓ **Q: How do I find my AWS Account ID?**  
👉 Run:
```bash
aws sts get-caller-identity
```
Copy the **"Account"** value and update `deploy_sagemaker.py`.

---

## **📢 Contributing**
Want to improve this project?  
Fork it, make changes, and submit a **Pull Request**! 🚀

**💡 Ideas for Improvement:**
- Add a **Dockerized version** for easy deployment.
- Implement **AutoML with SageMaker Hyperparameter Tuning**.
- Build a **React/Next.js frontend** for a better UI.

---

🔥 **Now go ahead and push this to GitHub!** 🚀  
```bash
git add .
git commit -m "Initial commit - CLV & Churn Prediction"
git push origin main
```

[def]: https://www.google.com/imgres?q=ML%20with%20aws%20project%20image&imgurl=https%3A%2F%2Fdaxg39y63pxwu.cloudfront.net%2Fimages%2Fblog%2Faws-ml-projects%2Faws_ml_projects.webp&imgrefurl=https%3A%2F%2Fwww.projectpro.io%2Farticle%2Faws-ml-projects%2F741&docid=dGl-TfHL5xEd_M&tbnid=kuA0S2nWefK3jM&vet=12ahUKEwjc8s6-5PWLAxWSFFkFHTQHG5EQM3oECGQQAA..i&w=480&h=288&hcb=2&ved=2ahUKEwjc8s6-5PWLAxWSFFkFHTQHG5EQM3oECGQQAA