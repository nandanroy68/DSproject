# Servomechanism Performance Prediction

## 📌 Project Overview
This project focuses on building a machine learning model to predict the rise time of a servomechanism. A servomechanism is a feedback control system used to control position, velocity, and acceleration. Using the classic **Servo Data Set**, this project analyzes how different component choices (motor, screw) and gain settings (P-gain, V-gain) impact the system's response time.

## 📂 Dataset
The dataset used in this project involves an extremely non-linear phenomenon. It typically contains the following attributes:

* **Motor:** Categorical (A, B, C, D, E) - The type of motor used.
* **Screw:** Categorical (A, B, C, D, E) - The type of screw mechanism.
* **Pgain:** Numerical (3, 4, 5, 6) - Proportional gain setting.
* **Vgain:** Numerical (1, 2, 3, 4, 5) - Velocity gain setting.
* **Class:** Numerical (Target) - The rise time of the mechanism.

## 🛠️ Technologies Used
* **Python:** Primary programming language.
* **Pandas:** For data manipulation and loading.
* **NumPy:** For numerical computations.
* **Matplotlib / Seaborn:** For data visualization and plotting relationships.
* **Scikit-Learn:** For data preprocessing (encoding), model building, and evaluation.

## 📓 Notebook Workflow (`servomechanism.ipynb`)
1.  **Data Loading:** Reading the raw dataset into a Pandas DataFrame.
2.  **Preprocessing:**
    * **One-Hot Encoding:** Converting categorical columns (`Motor`, `Screw`) into numeric values.
3.  **Exploratory Data Analysis (EDA):**
    * Analyzing the distribution of P-gain and V-gain.
    * Visualizing the correlation between different features and the target class.
4.  **Model Building:**
    * Splitting the data into Training and Testing sets.
    * Training models (Used Linear Regression but for better peformance we can also use Polynomial Regression or Random Forest Classifier etc.).
5.  **Model Evaluation:**
    * Predicting results on test data.
    * Calculating error metrics (MAE, MSE, Accuracy Score).

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/nandanroy68/DSproject.git](https://github.com/nandanroy68/DSproject.git)
    ```
2.  Navigate to the project directory:
    ```bash
    cd DSproject
    ```
3.  Install the necessary dependencies (if a requirements file is present, or install manually):
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
4.  Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
5.  Open `servomechanism.ipynb` and run the cells.

## 📈 Results
* The notebook demonstrates how categorical mechanical features influence the continuous performance metric of the servo.
* mean_absolute_error(y_test,model.predict(x_test)) = 7.190539677251235
* mean_squared_error(y_test,model.predict(x_test)) = 66.03589175595563
* r2_score(y_test,model.predict(x_test)) = 0.6807245170563927
* mean_absolute_percentage_error(y_test,model.predict(x_test)) = 0.8268204638174629 
     


## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/nandanroy68/DSproject/issues).

## 📝 License
This project is open-source and available under the [MIT License](LICENSE).
