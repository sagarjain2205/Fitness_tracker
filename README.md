# 💪  The Fitness Tracker (DSA Implementation)

A robust Command-Line Interface (CLI) application developed in Python to manage and analyze user workout progress, focusing on the practical implementation of core Data Structures and Algorithms (DSA).

## 🎯 Core Objective

The primary goal of this project is to demonstrate an efficient and intelligent **Fitness Tracking System** by strategically applying fundamental DSA principles for data storage, rapid lookup, and flexible user control.

---

## 🛠️ Technical Scope & DSA Highlights

| Data Structure / Algorithm | Feature Implemented | Time Complexity | Why it was Chosen |
| :--- | :--- | :--- | :--- |
| **Array/List (`daily_records`)** | Main Data Store | O(1) for access, O(n) for insertion | Chronological storage of daily records. |
| **Stack (`undo_stack`)** | **⏪ Workout Undo** Feature | **O(1)** (Constant Time) | Follows the **LIFO** (Last-In, First-Out) principle, ensuring the last entry is the first one undone. |
| **Binary Search** | **🔍 Progress Lookup** by Date | **O(log n)** (Logarithmic Time) | Provides **lightning-fast** searching capabilities, drastically improving performance for large datasets. |
| **Sorting (in `add_record`)** | Data Integrity | **O(n log n)** | A mandatory pre-condition to keep the `daily_records` list sorted by date, enabling the efficient Binary Search. |
| **Graphs (Matplotlib)** | **📊 Health Trends** Visualization | N/A | Converts raw data into visual trends for calories burned and duration over time. |

---

## ⚙️ Key Features

### 1. Robust Data Logging (Input Validation)
* Uses a safe `get_valid_input()` utility function with `try-except` blocks to handle non-numeric user entries gracefully, ensuring data integrity.

### 2. Efficient Data Management
* New records are inserted and the main list is **sorted immediately** (`daily_records.sort()`) to maintain the necessary structure for $O(\log n)$ lookups.

### 3. Quick Lookup by Date (Binary Search)
* Users can quickly check the details of any workout day by date. The algorithm efficiently divides the search space in half until the target record is found.

### 4. Reversible Actions (Stack)
* The `pop_from_undo_stack()` function allows users to instantly **reverse their last logged workout** entry, providing crucial flexibility and mistake correction.

### 5. Trend Analysis (Matplotlib)
* Generates line graphs to visualize the user's progress for **Calories Burned** and **Workout Duration** over the tracking period.

---

## 💻 How to Run the Project

### Prerequisites
* Python 3.x
* The `matplotlib` library:
    ```bash
    pip install matplotlib
    ```

### Execution
1.  Download or clone the repository.
2.  Open the `Fitness_tracker.ipynb` file in a Jupyter environment (JupyterLab, VS Code, etc.).
3.  Run all cells.
4.  The main menu will start, loading 5 days of dummy data for demonstration.

```bash
# Example Output:
=============================================
     💪 Fitness Tracker CLI - Group 42      
=============================================
1. ✍️ Log New Workout
2. 🔍 Look Up Progress by Date (Binary Search)
3. ⏪ Undo Last Workout Entry (Stack)
4. 📊 View Health Trend Graphs
5. 🚪 Exit
Enter your choice (1-5):-
```

### 🔮 Future Scope This project lays a solid DSA foundation that can be expanded with more advanced features:
- Hash Maps for User Profiles: Implement a Dictionary/Hash Map for $O(1)$ lookup time for user authentication and quick profile access.
- Queues for Future Plans: Introduce a Queue (FIFO) to manage a "Future Workout Plan" calendar, ensuring plans are pulled in the correct order.
- GUI: Transition the application from a Command-Line Interface to a modern Graphical User Interface (GUI) using libraries like Tkinter or PyQt.

Contact :
Email - jainsagar22105@gmail.com 
