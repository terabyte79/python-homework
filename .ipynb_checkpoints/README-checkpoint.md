# python-homework


## Source code for this assignment can be found under PyBank/main.ipynb

## Code used from instructor 

import os
import csv


current_dir = os.getcwd()
path_budget_data = os.path.join(current_dir, "budget_data.csv")

def read_csv_file(file_path):

    data = []
    with open(file_path,'r') as file:
        reader = csv.DictReader(file)
        for row in reader:
            data.append(dict((row)))
    return data

data = read_csv_file(path_budget_data)