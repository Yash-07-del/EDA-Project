# Airbnb Data Cleaning & Exploratory Data Analysis (EDA)

## 📌 Project Overview
This project performs an end-to-end **Exploratory Data Analysis (EDA)** on an Airbnb dataset. The primary goal is to perform data cleaning, handle structural anomalies, uncover key patterns, and create insightful data visualizations to understand the rental market dynamics, pricing distribution, and availability trends.

## 🧹 Data Cleaning & Preprocessing
Before diving into the analysis, the raw dataset was cleaned to ensure accuracy:
*   **Column Removal:** Removed unneeded administrative or index columns such as `Unnamed: 0`.
*   **Handling Duplicates:** Identified and dropped duplicate row entries across the dataset to protect data integrity.
*   **Handling Missing Values:** Cleaned critical text fields by removing rows missing essential metadata like listing `name` and `host_name`.
*   **Data Type Formatting:** Cleaned the text format of the `price` column by removing currency symbols (`$`) and casting the column into numerical floats and integers. 
*   **Date Conversions:** Converted string date fields (`Last_Review`, `Listing_Added`) into standard `datetime64[us]` objects.
*   **Categorical Standardization:** Fixed inconsistent formatting in the `room_type` column (e.g., standardizing mixed-casing and typos to 'Private Room', 'Entire Home/Apt', and 'Shared Room').
*   **Outlier Removal:** Used the **Interquartile Range (IQR) Method** to filter out extreme price outliers, establishing an accurate upper and lower pricing boundary for statistical analysis.

## 🛠️ Tech Stack & Dependencies
*   **Language:** Python
*   **Libraries:** 
    *   Data Manipulation: `pandas`, `numpy`
    *   Data Visualization: `matplotlib`, `seaborn`

## 📊 Key Visualizations & Insights
The notebook uses a mix of statistical plotting tools to visualize market attributes:
1.  **Price Boxplots & Violin Plots:** Built to compare data spreads before and after removing outliers, showcasing a more uniform view of normal listing rates.
2.  **Price Distribution Histograms:** Plots a Kernel Density Estimate (KDE) to visualize how the listing prices skew across the platform.
3.  **Availability & Review Trends:** Evaluates the annual availability (`Availability_365`) and timeline trends using line plots tracking both total reviews and new listing additions.
4.  **Categorical Analysis:** Employs count plots and bar plots to visualize total listings by room type and compare average pricing across those accommodations.
5.  **Geographical & Correlation Heatmaps:** Evaluates correlation matrices using heatmaps to reveal dependencies between pricing, room ratings, and accommodation size.

## 🚀 How to Run the Project
1.  Clone the repository:
    ```bash
    git clone https://github.com/Yash-07-del/EDA-Project.git
    cd EDA-Project
    ```
2.  Install the necessary libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

