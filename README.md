# 🩺 Diabetes Lifestyle & Blood Sugar Monitoring Program

This project is an interactive Python program that helps **people with diabetes** (or anyone monitoring their blood sugar) analyze how **lifestyle factors** such as sleep, stress, exercise, and diet irregularity affect their **daily glucose levels over time**.  

It combines **manual or dataset-based data entry** with **machine learning (Linear Regression)** to uncover correlations between habits and blood sugar, and provides **visual insights** into trends.

---

## Features
- **Flexible Data Entry**  
  - Option 1: Enter data manually (day-by-day)  
  - Option 2: Paste a 14-day dataset in a compact format for batch analysis  

- **Blood Sugar Rating Algorithm**  
  - Weighted average of:
    - Morning (fasting) blood sugar (**40%**)  
    - Post-meal average (**30%**)  
    - Before-bed sugar (**30%**)  

- **Lifestyle Tracking**  
  Records:
  - Sleep hours  
  - Stress level (1–10)  
  - Exercise minutes  
  - Irregular diet (yes/no)  

- **Machine Learning Analysis**  
  - Filters out irregular-diet days for cleaner insights  
  - Builds a **linear regression model** using lifestyle factors as predictors  
  - Outputs correlation coefficients showing which habits most strongly impact blood sugar  

- **Visual Reports**  
  - Bar chart of feature correlations  
  - Line chart comparing actual vs predicted blood sugar ratings  

---

## Example Workflow
1. Start the program and select **Manual Entry** or **Two-Week Dataset**  
2. Input daily readings + lifestyle data  
3. Program calculates a **Blood Sugar Rating** for each day  
4. Runs regression analysis on clean data (ignoring irregular-diet days)  
5. Displays:
   - **Mean Squared Error (MSE)**  
   - **R² score (model accuracy)**  
   - **Correlation strength of sleep, stress, and exercise**  
   - **Graphs** of results  

---

## Installation
Clone the repository and install requirements:

    git clone https://github.com/your-username/diabetes-blood-sugar-analysis.git
    cd diabetes-blood-sugar-analysis
    pip install -r requirements.txt

---

## Usage
Run the program:

    python main.py

Choose your data input method:  
- `1` → Manual daily entry  
- `2` → Paste 14-day dataset in format:  

    day--morning--post_breakfast--post_lunch--post_dinner--before_bed--sleep--stress--exercise--irregular_diet

Example:

    1--125--170--155--160--140--8.5--3--45--No|2--110--160--145--150--135--7.5--4--35--No|...

---

## Sample Outputs

**Correlation Results**  

    Mean Squared Error (MSE): 18.52
    R-squared (Model Accuracy): 82.13%
    Correlations:
    Sleep Hours: -1.2450
    Stress Level:  2.0356
    Exercise Minutes: -0.7644

**Graphs Produced**  
- Feature correlations (bar chart)  
- Predicted vs actual blood sugar ratings (line chart)  

---

## Project Structure

    diabetes-blood-sugar-analysis/
    │── main.py              # Main program file
    │── requirements.txt     # Python dependencies
    │── README.md            # Project documentation

---

## Tech Stack
- **Python 3.x**  
- **NumPy, Pandas** → data manipulation  
- **scikit-learn** → linear regression & evaluation metrics  
- **Matplotlib** → data visualization  

---

## Why This Matters
With diabetes on the rise globally, individuals often lack **personalized feedback** on how their lifestyle habits directly impact blood sugar. This project bridges that gap by:  
- Making data **easy to collect**  
- Using **machine learning** to find hidden patterns  
- Empowering users with **visual insights**  

---

## Future Improvements
- Add support for wearable/device data (continuous glucose monitors, smartwatches)  
- Expand to other ML models for prediction (Random Forest, Neural Nets)  
- Build a simple GUI or web app for non-technical users  
