# 📊 Predicting Employee Salaries with Linear Regression

This project demonstrates how to build a **Linear Regression Model** to predict employee salaries using IBM SPSS Modeler (or similar tools). The dataset contains details of 474 employees.

---

## 📁 1. Import and Examine the Data

### 🔹 Step 1: Load the Data
- From **Sources palette**, drag a `Var. File` node to a blank canvas.
- Edit the node, locate and select `employee_data.txt`.
- Click **OK** to confirm.

### 🔹 Step 2: Preview the Table
- From **Output palette**, connect a `Table` node to the `Var. File` node.
- Run the node to preview data.
- ➤ Dataset contains **474 employees**.

### 🔹 Step 3: Run Data Audit
- Connect a `Data Audit` node to the same source.
- Run it to inspect value distributions, types, and missing data.

---

## 🧪 2. Set Field Measurement Levels and Roles

### 🔸 Step 1: Add and Configure Type Node
- Add a `Type` node from **Field Ops**, connected to the `Var. File` node.
- Click **Read Values**.

### 🔸 Step 2: Configure Fields
- Set `educational_level` → **Ordinal**
- Set fields from `gender` to `months_previous_experience` → **Input**
- Set `current_salary` → **Target**

---

## 📈 3. Create and Train Linear Regression Model

### 🔹 Step 1: Add Linear Model
- Add a `Linear` node from the **Modeling palette** connected to the `Type` node.

### 🔹 Step 2: Edit Build Options
- Go to **Build Options** tab:
  - Under **Basics**: Uncheck `Automatically prepare data`.
  - Under **Model Selection**: Choose `Include all predictors`.

### 🔹 Step 3: Train the Model
- Click **Run** to build the model.

---

## 📊 4. Evaluate the Model

### 🔸 View Model Summary
- Edit the model nugget and click **Model Summary**.

### 🔸 View Predictor Importance
- Click **Predictor Importance**
  - `job_category` → Most important predictor
  - `gender` → Second most important
  - `region` and `age` → Least important

### 🔸 Visualize Predictions
- Click **Predicted by Observed**
  - ➤ Predicted values show two major clusters rather than a smooth trend.

### 🔸 View Coefficients
- Click **Coefficients by Observed**
- From the **Style** dropdown, select `Table`.

---

## ✅ Summary

You now have a working linear regression model that:
- Uses job role, education, experience, and other features
- Identifies job category and gender as major salary predictors
- Can be used to further explore wage inequality or HR planning


