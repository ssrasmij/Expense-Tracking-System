# Expense Management System

This project is an **Expense Management System** that combines a **Streamlit frontend application** with a **FastAPI backend server**. It allows users to efficiently track and analyze their expenses by date, category, and month.

---

## 🚀 Features

- 📅 **Add or Update Expenses**: Input daily expenses with categories and notes.
- 📊 **View Analytics by Category**: Visualize spending breakdown for specific date ranges.
- 📈 **View Analytics by Month**: Visualize monthly expenses year by year.
- 🛡️ **Backend API**: Easily fetch, update, and analyze expenses using FastAPI.

---

## 📂 Project Structure

```
├── frontend/		# Contains the Streamlit application code
├── backend/		# Contains the FastAPI backend server code
├── tests/		# Contains unit tests for both frontend and backend
├── .env
├── requirements.txt	# Lists required Python packages
├── README.md		# Project overview and setup instructions
```

---

## ⚙️ Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/expense-management-system.git
   cd expense-management-system
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the FastAPI server:** (Navigate to the `backend` directory first)
   ```bash
   cd backend
   uvicorn server:app --reload
   ```

4. **Run the Streamlit app:** (Navigate to the `frontend` directory first)
   ```bash
   cd ../frontend
   streamlit run app.py
   ```
---

## 🎮 How to Use the App

### 1. **Add or Update Expenses**
- Navigate to the **Add/Update** tab.
- The default date is set to today’s date.
- Input expenses under the following categories:
  - Rent
  - Food
  - Shopping
  - Entertainment
  - Other
- Click **Submit** to save your expenses for that date.

### 2. **View Analytics by Category**
- Go to the **Analytics By Category** tab.
- Select a **Start Date** and an **End Date**.
- Click **Get Analytics** to view:
  - Total spending in each category
  - Percentage breakdown of expenses
- A bar chart and detailed table will display your expense distribution.

### 3. **View Analytics by Month**
- Go to the **Analytics By Months** tab.
- View separate graphs for each year showing monthly expenses.
- Review a breakdown of your spending month-by-month.

---

## 📌 API Endpoints

### 🔍 Fetch Expenses
- **GET** `/expenses/{expense_date}`
- **Description:** Retrieves expenses for the specified date.

### 📋 Fetch All Expenses
- **GET** `/all-expenses/`
- **Description:** Retrieves all recorded expenses.

### ➕ Add or Update Expenses
- **POST** `/expenses/{expense_date}`
- **Body:** List of expenses for the given date.

### 📊 Analytics by Category
- **POST** `/analytics-by-category/`
- **Body:** Date range (`start_date`, `end_date`) for analysis.

### 📅 Analytics by Month
- **GET** `/analytics-by-month/`
- **Description:** Retrieves total expenses grouped by month and year.

---

Enjoy tracking your expenses! 💰

