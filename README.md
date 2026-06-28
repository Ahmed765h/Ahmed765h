# AI Financial Risk Prediction System

![Banner](screenshots/banner.png) <!-- Placeholder for a professional banner -->

## 🚀 Project Overview

This project develops an **AI Financial Risk Prediction System** designed to assist financial institutions in making informed decisions regarding loan approvals, credit risk assessment, and default likelihood. By leveraging advanced Machine Learning algorithms and Explainable AI (XAI) techniques, the platform provides accurate predictions and transparent insights into the factors driving financial risk.

## 🎯 Business Problem

Financial institutions face significant challenges in accurately assessing the risk associated with lending. Traditional methods can be subjective, time-consuming, and may not fully capture complex patterns in financial data. This leads to potential losses from defaults or missed opportunities with creditworthy customers. This system aims to mitigate these risks by providing a data-driven, AI-powered solution for more precise and efficient risk evaluation.

## 💡 Solution

The AI Financial Risk Prediction System offers a comprehensive solution by:

-   **Automating Risk Assessment**: Utilizing ML models to predict loan approval probability, customer credit risk, and default likelihood.
-   **Enhancing Decision-Making**: Providing financial risk scores and actionable insights to support loan officers and risk managers.
-   **Ensuring Transparency**: Incorporating Explainable AI (SHAP) to clarify why a particular risk prediction was made.
-   **Streamlining Operations**: Offering an interactive dashboard and a robust API for seamless integration into existing workflows.

## ⚙️ Machine Learning Pipeline

1.  **Data Ingestion**: Uploading financial datasets (CSV) containing customer and loan information.
2.  **Data Preprocessing**: Automatic handling of missing values, feature scaling, and one-hot encoding for categorical variables.
3.  **Feature Engineering**: Creation of new features to enhance model performance.
4.  **Model Training**: Training multiple classification models (Logistic Regression, Random Forest, XGBoost, LightGBM, CatBoost) to predict risk.
5.  **Model Selection**: Identifying the best-performing model based on metrics like ROC AUC, tracked via MLflow.
6.  **Prediction & Scoring**: Generating loan approval probabilities, default likelihoods, and comprehensive financial risk scores.
7.  **Explainability**: Applying SHAP (SHapley Additive exPlanations) to interpret model predictions and understand feature importance.

## 📊 Model Comparison

The platform supports training and comparing various state-of-the-art machine learning models. MLflow is used to track experiments, parameters, and metrics, allowing for an objective comparison and selection of the most suitable model for financial risk prediction.

## 🧠 Explainable AI (XAI) with SHAP

Understanding *why* a model makes a certain prediction is crucial in financial applications. This system integrates SHAP values to provide local and global interpretability:

-   **Local Explanations**: For each individual prediction, SHAP values illustrate how each feature contributes to the final risk score, helping to justify loan decisions.
-   **Global Explanations**: SHAP summaries reveal overall feature importance, highlighting which factors are most influential across the entire dataset in determining financial risk.

## 🚀 Installation

To set up and run the project locally, follow these steps:

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/YOUR_USERNAME/ai-financial-risk-prediction.git
    cd ai-financial-risk-prediction
    ```
2.  **Build and run with Docker Compose**:
    ```bash
    docker-compose up --build
    ```
    This will start both the FastAPI (on port 8000) and Streamlit dashboard (on port 8501).

3.  **Access the applications**:
    -   FastAPI: `http://localhost:8000`
    -   Streamlit Dashboard: `http://localhost:8501`
    -   MLflow UI: `http://localhost:5000` (if MLflow tracking server is configured to run separately)

## 📖 API Documentation

The FastAPI includes automatically generated interactive API documentation (Swagger UI) available at `http://localhost:8000/docs` once the API service is running.

## 📸 Dashboard Preview

![Dashboard Overview](screenshots/dashboard_overview.png)
*An overview of the interactive Streamlit dashboard, showcasing risk score distribution, loan approval predictions, and feature importance.*

![SHAP Explainability](screenshots/shap_explainability.png)
*A visualization of SHAP values explaining individual predictions, highlighting feature contributions.*

## 🛠️ Technologies Used

-   **Backend**: Python 3.11, FastAPI
-   **Frontend**: Streamlit
-   **Machine Learning**: Scikit-learn, XGBoost, LightGBM, CatBoost, Pandas, NumPy
-   **Explainable AI**: SHAP
-   **Data Visualization**: Plotly
-   **MLOps**: MLflow
-   **Database**: SQLite (for MLflow tracking)
-   **Containerization**: Docker, Docker Compose

## 📂 Folder Structure

```
ai-financial-risk-prediction/
├── app/                  # Streamlit application code
├── api/                  # FastAPI application code
├── models/               # Trained ML models and model-related utilities
├── dashboard/            # (Optional) Additional dashboard components or assets
├── data/                 # Sample and raw datasets
├── notebooks/            # Jupyter notebooks for EDA, model development
├── screenshots/          # Images for README and documentation
├── docs/                 # Additional documentation files
├── tests/                # Unit and integration tests
├── requirements.txt      # Python dependencies
├── Dockerfile            # Docker build instructions
├── docker-compose.yml    # Docker Compose configuration
├── LICENSE               # Project license
├── .gitignore            # Files/directories to ignore in Git
└── README.md             # Project overview and documentation
```

## 🔮 Future Improvements

-   Integration with real-time data sources for continuous risk monitoring.
-   Implementation of advanced XAI techniques beyond SHAP.
-   User authentication and role-based access control for the dashboard and API.
-   Automated retraining pipelines for models to adapt to new data.
-   Support for different financial products and risk types.
-   Deployment to cloud platforms (AWS, Azure, GCP) for scalability and production readiness.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
