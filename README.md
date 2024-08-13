# Python Data Engineer / Analyst Interview Questions

Welcome to the Python Data Engineer / Analyst Interview Questions repository! This collection of Python examples is designed to help you prepare for interviews by providing a variety of practical examples using the `numpy` and `pandas` libraries. Each example is accompanied by sample data and a detailed answer.

## Data Setup

Create the `departments` and `employees` datasets.

<details><summary>
:arrow_forward: View Code
</summary>
  
  ```code
import pandas as pd

# Sample data for employees
employees = pd.DataFrame({
    'employee_id': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12],
    'first_name': ['John', 'Jane', 'Jim', 'Jake', 'Jill', 'Joe', 'Jerry', 'Jenny', 'Jordan', 'Jamie', 'John', 'Jamie'],
    'last_name': ['Doe', 'Smith', 'Brown', 'White', 'Green', 'Black', 'Red', 'Blue', 'Purple', 'Orange', 'Doe', 'Orange'],
    'department_id': [1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 1, 2],
    'salary': [50000, 60000, 55000, 45000, 70000, 80000, 75000, 65000, 48000, 67000, 50000, 67000],
    'hire_date': pd.to_datetime(['2020-01-15', '2019-03-10', '2018-07-23', '2021-06-12', '2017-11-19', 
                                  '2015-04-29', '2016-09-14', '2019-12-25', '2020-08-05', '2018-05-21', 
                                  '2020-01-15', '2018-05-21']),
    'manager_id': [None, 1, 1, 3, None, 2, 3, 4, 5, 6, None, 6]
})

# Sample data for departments
departments = pd.DataFrame({
    'department_id': [1, 2, 3, 4, 5],
    'department_name': ['HR', 'Finance', 'IT', 'Marketing', 'Civil']
})

print("Employees DataFrame:")
print(employees)

print("\nDepartments DataFrame:")
print(departments)
```
</details> 
<br> 

## 1: Finding the MAX and MIN salary from the employees table

<br>

### a. Finding the top 2 maximum and minimum salaries❓

<details><summary>
:arrow_forward: View Answer
</summary>

  ```code
# Finding 2 max and 2 min salaries
top_2_max = employees.nlargest(2, 'salary')
top_2_min = employees.nsmallest(2, 'salary')

# Adding 'salary_type' column
top_2_max['salary_type'] = 'Max'
top_2_min['salary_type'] = 'Min'

# Concatenating results
top_2_max_and_min = pd.concat([top_2_max, top_2_min])

print(top_2_max_and_min)
```
</details> 
<br> 

### b. Finding the top 2 maximum salaries of each department❓

<details><summary>
:arrow_forward: View Answer
</summary>

  ```code
```
</details> 
<br> 

### c. Finding the top 2 minimum salaries of each department❓

<details><summary>
:arrow_forward: View Answer
</summary>

  ```code
```
</details> 
<br> 
