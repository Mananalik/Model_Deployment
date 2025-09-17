# Machine Learning Model Deployment

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://model-deployment-5-n04s.onrender.com/)

This project is a demonstration of deploying a machine learning model as a web service using Python and the Flask framework. The application is hosted on Render.

**Live Application URL:** [https://model-deployment-5-n04s.onrender.com/](https://model-deployment-5-n04s.onrender.com/)

---

### Description

This web service exposes a pre-trained scikit-learn model through a REST API. It accepts input data in JSON format, passes it to the model for inference, and returns the prediction.

*(**Note:** You should add a sentence here describing what your model actually predicts, e.g., "This model predicts housing prices based on features like area and number of bedrooms.")*

---

### Tech Stack

* **Python 3.10**
* **Flask:** A micro web framework for the API.
* **Scikit-learn:** For the machine learning model.
* **Gunicorn:** A production-ready WSGI server.
* **Render:** The cloud platform for deployment.

---

### How to Run Locally

To set up and run this project on your local machine, follow these steps.

**Prerequisites:**
* Git
* Conda (for environment management)

**Installation:**

1.  **Clone the repository:**
    ```bash
    git clone <https://github.com/Mananalik/Model_Deployment>
    cd <Model_Deployment>
    ```

2.  **Create and activate the Conda environment:**
    The project requires Python 3.10.
    ```bash
    conda create -n ml_project python=3.10
    conda activate ml_project
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Flask development server:**
    ```bash
    flask run
    ```
    The application will be available at `http://127.0.0.1:5000`.

---

### API Usage

You can interact with the API using any HTTP client like `curl` or Postman.

**Endpoint:** `/predict`
**Method:** `POST`
**Body:** JSON object with your model's input features.

**Example using `curl`:**

*(**Note:** You must replace the `key` and `value` placeholders below with the actual feature names and data your model expects.)*

```bash
curl -X POST \
-H "Content-Type: application/json" \
-d '{"feature1": 10, "feature2": 5.5, "feature3": 2}' \
[https://model-deployment-5-n04s.onrender.com/predict](https://model-deployment-5-n04s.onrender.com/predict)
