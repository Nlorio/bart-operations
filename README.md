# BART_operations

Project Repository for BART Make and Break problem. An optimization solution to schedule the daily make and break operations of BART.

## Notebooks

- steadyStateModel_baseline.ipynb:
  - Large linear program. Loads and structures pre-processed data. Optimizes for cost while adhering to a complex set of inventory, demand, and manpower constraints across the BART system. Determines optimal number of makes/breaks, the total costs, operating costs per mile, yard team costs, and the make/break costs. Exports results for easier analysis. Runs sensitivity analysis on model paramaters. 
  
 - steadyStateModel_all10.ipynb:
  - Large linear program. Performs same functions as above notebook. Runs the model assuming all consists are 10 cars in length. 
  
  - steadyStateModel_green.ipynb:
    - Large linear program. Performs same functions as above notebook. Runs the model with a focus on minimizing operating hours for consists in the system. 

## Data 



### Pre-Processing NoteBooks

- format_BART_Schedule.ipynb
  -

- PreProcessData_v3.ipynb
  - 

## Presentation

See presentation directory. 

## Report 

See report directory. 


