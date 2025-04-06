# House Price Prediction with MLOps

This project showcases a comprehensive Machine Learning (ML) pipeline designed for production, highlighting best practices in MLOps. It integrates MLflow and ZenML to manage experiments, track models, and streamline the deployment process. The model predicts house prices using various features, and the entire process—from data ingestion to deployment—is organized with a focus on scalability, maintainability, and robust ML operations.

## Key Features

- **End-to-End ML Pipeline**: The project takes a simple house price prediction model all the way from data preprocessing to deployment.
- **MLflow & ZenML Integration**: MLflow is used for experiment tracking, while ZenML orchestrates the ML pipeline, allowing seamless integration with various components.
- **Best Practices for MLOps**: The project emphasizes best practices for ML model management, continuous experimentation, and version control for models and pipelines.
- **Design Patterns**: The project incorporates well-known design patterns, including the **Factory** and **Template** design patterns, to make the codebase flexible, reusable, and easy to maintain.

## Design Patterns

### 1. Factory Design Pattern

The **Factory Design Pattern** is used to encapsulate the creation of different components (e.g., pre-processing steps, models) so that the system can remain flexible when adding or modifying components in the future. This ensures that the creation logic for these objects is centralized and abstracted, making the code more modular and easier to extend.

### 2. Template Design Pattern

The **Template Design Pattern** is employed in the ML pipeline to define the skeleton of the model-building process while allowing subclasses to fill in the specifics. This pattern ensures that the core pipeline structure remains unchanged, while the individual steps—such as data preprocessing and model training—can be customized as needed. It also improves reusability, as the general flow is predefined, and only the specific implementation of the steps is altered.

## Setup & Installation

To get started with this project, follow these steps:

### 1. Clone the repository

```bash
git clone https://github.com/your-username/house-price-prediction.git
cd house-price-prediction
```

### 2. Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up MLflow and ZenML

Make sure that MLflow and ZenML are properly set up to track experiments and manage your pipeline. You can start MLflow by running:

```bash
mlflow ui --host 127.0.0.1 --port 5000
```

### 5. Run the pipeline

To start the house price prediction pipeline, use the following ZenML command:

```bash
zenml pipeline run house_price_pipeline
```

## Best Practices

- **Modularity**: The pipeline is designed to be modular, with clear separation of concerns between preprocessing, model training, and deployment. This makes the code easy to maintain and scale.
- **Experiment Tracking**: MLflow is used for tracking experiments, allowing you to log hyperparameters, metrics, and models, and to track changes over time.
- **Version Control for Models**: All models are versioned, ensuring that you can always revert to previous versions if needed.
- **Code Reusability**: The use of the Factory and Template design patterns makes the code highly reusable, allowing for easy updates and integration of new models or steps.

## Conclusion

This project provides a solid foundation for building and deploying machine learning models in a production environment. By integrating ZenML and MLflow, it demonstrates the best practices for managing ML experiments, tracking models, and organizing the code for scalability and maintainability.

Feel free to explore the code, experiment with the pipeline, and extend the project with your own models or features!
