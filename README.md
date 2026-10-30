# FinE Data Analytics Assignment

Classifies line items (for example "Revenue from operations") into their **Format Classification** and **Classification of Item**. It uses TF-IDF features from the item name and two **Random Forest** models. Rows that are missing a label are filled in automatically, and the result is saved back to Excel.

## How to run (step by step)

You need **Python 3.10 or newer** ([download](https://www.python.org/downloads/)). No API key is needed, and the Excel data file is included.

**1. Download the project**

```bash
git clone https://github.com/amitmohanty022/FinE-Data-Analytics-Assignment.git
cd FinE-Data-Analytics-Assignment
```

**2. Create a virtual environment and activate it**

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

**3. Install the requirements**

```bash
pip install -r requirements.txt
```

**4. Start Jupyter and run the notebook**

```bash
jupyter notebook "Fine_Data_Analytics_(Final) (1).ipynb"
```

Choose **Run → Run All Cells**.

## What the notebook does

1. Loads `Item-Format-Classification-Assignment(Main) (1) (1).xlsx` (780 items).
2. Splits rows into labelled (used for training) and unlabelled (to predict).
3. Turns `Name Of Item` into TF-IDF features.
4. Trains one Random Forest for `Format Calssification` and one for `Classification of Item`, and prints validation accuracy.
5. Fills in the missing labels and saves `Item-Format-Classification-Assignment(Main).xlsx`.

> The included Excel file is already fully labelled, so step 5 reports "No unlabelled rows to predict". To try it yourself, clear some cells in the two classification columns and run the notebook again.
