# Smart Expense Analyzer

**Day 31 – Python Data Analytics Coding Challenge**

A beginner-friendly Python project that uses arithmetic, comparison, logical, and assignment operators to analyze a user's monthly expenses and determine their financial status.

---

## Objective

Analyze a monthly budget and answer:

- How much was spent in total?
- How much was saved?
- How do certain expenses compare to each other?
- Is the saving level good, average, or low?
- What happens to savings capacity after a salary bonus?

## Input Data

| Variable        | Amount (₹) |
|-----------------|-----------:|
| `salary`        | 50,000     |
| `rent`          | 12,000     |
| `food`          | 8,000      |
| `transport`     | 3,000      |
| `entertainment` | 4,000      |

## Tasks and Concepts

| # | Task                       | Operator Type        | Description                                                              |
|---|----------------------------|----------------------|--------------------------------------------------------------------------|
| 1 | Total Expenses             | Arithmetic (`+`)     | Sum rent, food, transport, and entertainment                             |
| 2 | Savings Calculation        | Arithmetic (`-`)     | `savings = salary - total_expenses`                                      |
| 3 | Expense Comparison         | Comparison (`>`, `<`)| Is rent > food? Is transport < entertainment?                            |
| 4 | Financial Condition Check  | Logical (`and`, `or`)| Classify savings as Good, Average, or Low                                |
| 5 | Bonus Update               | Assignment (`+=`)    | Increase salary by 10%                                                   |

### Savings Classification Rules (Task 4)

| Savings Range        | Result            |
|----------------------|-------------------|
| Greater than 10,000  | **Good Saving**   |
| 5,000 to 10,000      | **Average Saving**|
| Less than 5,000      | **Low Saving**    |

## Results

| Output                              | Value          |
|-------------------------------------|----------------|
| Total Expenses                      | 27,000         |
| Savings                             | 23,000         |
| Is rent greater than food?          | `True`         |
| Is transport less than entertainment? | `True`       |
| Financial Condition                 | Good Saving    |
| Salary after 10% bonus              | 55,000.0       |

## Project Structure

```
.
├── Day-31-Data-analytics-challenge-python.ipynb   # Solution notebook
├── Day31_Coding_Challenge.pdf                     # Challenge problem statement
└── README.md                                      # Project documentation
```

## How to Run

1. **Install Python 3.9+** and Jupyter:
   ```bash
   pip install notebook
   ```
2. **Launch Jupyter Notebook** from the project folder:
   ```bash
   jupyter notebook
   ```
3. Open `Day-31-Data-analytics-challenge-python.ipynb`.
4. Run all cells in order (**Kernel → Restart & Run All**).

## Code Snapshot

```python
# Task 1: Total expenses
Total_expenses = rent + food + transport + entertainment

# Task 2: Savings
savings = salary - Total_expenses

# Task 3: Comparisons
print(rent > food)
print(transport < entertainment)

# Task 4: Financial condition
if savings > 10000:
    print("Good Saving")
elif savings < 10000 and savings > 5000:
    print("Average Saving")
else:
    print("Low Saving")

# Task 5: Bonus
salary = salary + (salary * 10 / 100)
```

## Possible Improvements

- **Include boundary values in Task 4.** The current `elif` uses strict `<` and `>`, so savings of exactly 5,000 or 10,000 would fall through to "Low Saving". Using `5000 <= savings <= 10000` fixes this.
- **Use the assignment operator for Task 5.** The challenge asks for `salary += salary * 0.10`, which does the same thing as the current line.
- **Follow Python naming conventions.** Use `total_expenses` (lowercase) instead of `Total_expenses`.
- **Make it interactive.** Accept expenses via `input()` so any user can analyze their own budget.
- **Extend the analysis.** Add expense percentages of salary, or a chart of spending by category.

## Skills Practiced

- Python variables and data types
- Arithmetic, comparison, logical, and assignment operators
- Conditional statements (`if` / `elif` / `else`)
- Printing formatted output
- Working in Jupyter Notebook

## Author

Ch Sai Sireesha
