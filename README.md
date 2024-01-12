# Knapsack Problem Solver

## Overview
This Python program provides a solution to the 0/1 Knapsack Problem using dynamic programming. The problem involves optimizing the selection of items with given weights and values to maximize the total value without exceeding a predefined weight capacity.

## Algorithm
### 1. Problem Definition
Given a set of items with weights and values, the goal is to select a subset of items to maximize the total value while not exceeding a specified weight capacity.

### 2. Algorithm Overview
The solution employs a dynamic programming approach with the following steps:

#### 2.1 Finding Breakpoint (b)
Identify the index where the cumulative sum of weights first exceeds the capacity.

#### 2.2 Initializing Matrix (S)
Create a matrix to store intermediate results. Rows represent items, and columns represent possible weights.

#### 2.3 Initialization for Breakpoint (b)
Set specific values in the matrix based on the identified breakpoint.

#### 2.4 Dynamic Programming Loop
- **Copy Values from the Previous Row:** Copy values from the row above in the matrix.
- **Updating Values Based on Weights:** Update values based on weights to explore possible solutions.
- **Further Updates Based on Weights:** Additional updates based on weights to refine the solution.

#### 2.5 Finding the Optimal Solution
Determine the maximum value achievable.

### 3. How to Use
1. Run the program.
2. Input weights and capacity when prompted.

### 4. Example Usage
```python
# Example Usage
custom_weights = [2, 4, 6, 8, 2]
custom_C = 9

optimal_solution, S_matrix, breakpoint, wbar, r, column_C_values = algorithm_example(custom_weights, custom_C)

# Displaying the result with additional conditions
if breakpoint == 0 or not any(column_C_values):
    print("Optimal Solution: False")
else:
    print("Optimal Solution: True")
print("Breakpoint Index (b):", breakpoint)
```

### Results
View the results, including the optimal solution, breakpoint index, and the dynamic programming table.

### Contributing
Contributions are welcome. Please follow the Contribution Guidelines.

### License
This project is licensed under the MIT License.

This README includes a table of contents to help users navigate through the document more easily.
