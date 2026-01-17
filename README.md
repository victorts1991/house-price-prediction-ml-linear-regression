# 🏠 House Price Prediction - Linear Regression Study

This repository presents the implementation and technical documentation of a **Linear Regression** algorithm for analyzing and predicting real estate values. The focus is on demonstrating the architecture behind the model and the interpretation of its mathematical parameters.

## 🚀 Application Scenario & Future Vision
Although this model was trained using the *California Housing* dataset (focused on **purchase** values in the USA), the engineering logic applied here can be extended to a Brazilian ecosystem:

* **Integrated Web Scraping**: Capturing raw data from real estate portals like QuintoAndar or VivaReal.
* **Budget Filtering**: The model can predict which cities or neighborhoods (e.g., in Bahia) have properties that fit within a user's spending ceiling.
* **Necessary Adaptations**: To implement a rental scenario in Brazil, the model would need to be re-trained with specific local data, such as inflation indices (IGP-M/IPCA) and regional rental values.

---

## 🧠 The Algorithm: Linear Regression
The project utilizes **Linear Regression** to find the "line of best fit" that describes the relationship between variables such as Median Income and Price.

* **Intercept (b)**: The "initial state" or base value of the graph before variables enter the calculation. It acts as an offset to align the line with real-world data.
* **Coefficients (w)**: The weight of each attribute. We mathematically identified that **Median Income (MedInc)** is the most consistent predictor.
* **Ordinary Least Squares (OLS)**: The optimization method used internally by Scikit-Learn to minimize the distance (error) between real points and model predictions.

---

## 🛠️ Technologies Used
* **Python 3.x**: Core language for development.
* **Pandas**: Data manipulation and Exploratory Data Analysis (EDA).
* **Scikit-Learn**: Machine Learning library for training, data splitting, and evaluation.
* **Matplotlib / Seaborn**: Data visualization and creation of the correlation matrix.
* **Jupyter Notebook**: Interactive development environment used for the project.

---

## 📊 Model Performance
Based on tests performed with 20% of the dataset (data never seen by the model), the results were:

* **MSE (Mean Squared Error): 0.5559**
* **R² Score: 0.5758**

This means the model explains approximately **57.58%** of the price variation based on the provided data, providing a solid baseline for a linear model.

---

## ⚙️ How to Run in Visual Studio Code

Since the project uses a fixed dependency file (`freeze`), follow these steps to set up your environment:

1.  **Clone the repository**:
2.  **Create and Activate a Virtual Environment (VENV)**:
    ```bash
    python -m venv venv
    # On Windows: .\venv\Scripts\activate
    # On Mac/Linux: source venv/bin/activate
    ```
3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
4.  **Select the Kernel**: In VS Code, open the `.ipynb` file, click on **"Select Kernel"** in the top right corner, and choose the `venv` environment you just created.

---

## 📊 How to Run in Google Colab
1.  Access [Google Colab](https://colab.research.google.com/).
2.  Go to `File > Upload Notebook` and upload the `.ipynb` file from this repository.
3.  Colab comes with the necessary libraries pre-installed; simply run the cells.

