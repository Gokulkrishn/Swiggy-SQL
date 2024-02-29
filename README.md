# Swiggy-SQL

DataSet: https://docs.google.com/spreadsheets/d/1JgNHxTixDA50W1l6pNFmHKRaX1a9QnXrpGLsJtzo6Gg/edit#gid=0


import pandas as pd

# Load the Excel file
excel_file_path = 'your_excel_file.xlsx'
excel_file = pd.ExcelFile(excel_file_path)

# Iterate through each sheet and save it as a separate CSV file
for sheet_name in excel_file.sheet_names:
    df = excel_file.parse(sheet_name)
    new_file_name = f"{sheet_name}.csv"
    df.to_csv(new_file_name, index=False)
    print(f"{sheet_name} saved as {new_file_name}")



Question:
Swiggy Case Study-

1. Find customers who have never ordered
2. Average Price/dish
3. Find the top restaurant in terms of the number of orders for a given month
4. restaurants with monthly sales greater than x for 
5. Show all orders with order details for a particular customer in a particular date range
6. Find restaurants with max repeated customers 
7. Month over month revenue growth of swiggy
8. Customer - favorite food

Homework
Find the most loyal customers for all restaurant
Month over month revenue growth of a restaurant
Most Paired Products
