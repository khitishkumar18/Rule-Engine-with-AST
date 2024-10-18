
# 🌟 **Rule Engine Application** 🌟

## 🚀 Overview
This is a simple **3-tier rule engine application** that determines user eligibility based on attributes like **age**, **department**, **income**, and **spend**. The system uses an **Abstract Syntax Tree (AST)** to represent conditional rules and allows for dynamic creation, combination, and modification of these rules.

### 🖼️ **Main Project Overview Image**
> ![Screenshot 2024-10-18 230850](https://github.com/user-attachments/assets/dda86de7-f5dd-48c5-81d9-9cc4e4084664)


---

## ✨ Features
- **🛠️ Create Rule**: Allows users to create rules based on given attributes.
- **🔗 Combine Rules**: Combines multiple rules into a single AST.
- **✅ Evaluate Rule**: Evaluates the given data against the rule and returns whether the user is eligible.
- **⚠️ Error Handling (Bonus)**: Handles invalid rule strings and data formats, providing meaningful error messages to the user.

### 🖼️ **UI: Create Rule Feature**
> *(Add an image here showcasing the UI for creating a rule. This could include a screenshot of the "Create Rule" form with an example rule.)*

---

## 🏗️ Project Structure
```
app/
│
├── api.py          # Provides API functions to interact with the rule engine.
├── ast.py          # Defines the AST data structure.
├── database.py     # Handles database initialization and operations.
├── rules.py        # Implements rule creation, combination, and evaluation logic.
│
├── static/         # Contains static files (CSS, JavaScript).
│   ├── css/
│   │   └── style.css     # CSS styles.
│   └── js/
│       └── script.js     # JavaScript files.
│
└── templates/
    └── index.html   # Main UI template.
    
tests/
│
├── test_rules.py    # Unit tests for rule creation, combination, and evaluation.
└── test_api.py      # Unit tests for the API functions.

requirements.txt     # Lists dependencies.
main.py              # Entry point of the application.
README.md            # This documentation file.
```

---

## 💡 Design Choices
- **🔄 3-tier Architecture**: Separates the UI, API, and backend logic for better maintainability and scalability.
- **🌳 Abstract Syntax Tree (AST)**: Represents conditional rules, allowing for dynamic creation, combination, and modification.
- **🛡️ Error Handling**: Comprehensive error handling ensures robustness for invalid rule strings and data formats.
- **🎨 UI Design**: The UI is clean and user-friendly, providing dynamic feedback for rule evaluation results.

---

## ⚙️ Instructions

### Prerequisites
- 🐍 Python 3.6 or higher
- 🧩 Flask
- 🗃️ SQLite (for database)

### 🏗️ Build and Install
1. **Create a virtual environment**:
   ```bash
   python -m venv venv
   ```
   
2. **Activate the virtual environment**:
   ```bash
   venv/Scripts/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Initialize the database**:
   ```bash
   python -c "from app.database import initialize_database; initialize_database()"
   ```

5. **Run the application**:
   ```bash
   python main.py
   ```

   Open your web browser and go to `http://127.0.0.1:5000/`.

---

## 🧪 Test

### 🛠️ Sample Tests to Try on UI
1. **Creating the rule**:
   ```bash
   ((age > 30 AND department = 'Sales') OR (age < 25 AND department = 'Marketing')) AND (salary > 50000 OR experience > 5)
   ```

   Input the above rule in the "Create Rule" text box and press the **Create Rule** button. It will prompt a success message and generate the relevant AST (autofilled).

### 🖼️ **Rule Creation Success**
> *(Add an image here showcasing the success message after creating a rule.)*

---

2. **Input a query to evaluate**:
   ```json
   {
     "age": 50,
     "department": "Sales",
     "salary": 60000,
     "experience": 10
   }
   ```

   Input this JSON in "Data (JSON format):" and press **Evaluate**. It will return either **True** or **False** based on the rule.

### 🖼️ **AST Representation Example**
> *(Add an image here that displays the generated AST from the rule creation process.)*

### 🖼️ **Input Query Example**
> *(Add an image here showing an example input query in JSON format.)*

### 🖼️ **Evaluation Result (True/False)**
> *(Add an image here showing the result of a query evaluation — either True or False.)*

---

## 🧩 Predefined Test Cases:
To run the tests, or directly browse it on the web browser with the provided examples:

```bash
python -m unittest discover tests
```

---

