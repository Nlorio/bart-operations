# BART_operations

Project Repository for BART Make and Break problem. An optimization solution to schedule the daily make and break operations of BART.

## Notebooks

- steadyStateModel_baseline.ipynb:
  - Large linear program. Loads and structures pre-processed data. Optimizes for cost while adhering to a complex set of inventory, demand, and manpower constraints across the BART system. Determines optimal number of makes/breaks, the total costs, operating costs per mile, yard team costs, and the make/break costs. Exports results for easier analysis. Runs sensitivity analysis on model paramaters. 
  
 - steadyStateModel_all10.ipynb:
   - Large linear program. Performs same functions as above notebook. Runs the model assuming all consists are 10 cars in length. 
  
  - steadyStateModel_green.ipynb:
    - Large linear program. Performs same functions as above notebook. Runs the model with a focus on minimizing operating hours for consists in the system. 

## Assumptions

- Consists will contain only 5 or 10 cars.
- The 1,081 train cars will all be either D or E cars.
- The system layout is the same as it currently is (i.e. no Berryessa extension and no yard
openings/closures).
- There will be a 2:3 ratio of D to E cars
- Fleet consists of 5-car modules that can move independently, and two such modules can be
coupled and decoupled (DEEEDDEEED → DEEED + DEEED).
- Power and maintenance costs are both linear functions of the distance a train car travels.
- Makes and breaks only occur at yards or tail tracks at the end of a route (i.e. a train traveling from
- Warm Springs to Richmond will not stop at the Hayward yard to be shortened or lengthened).
- There will always be enough yard/tail track space for a make/break to be carried out.
- Inventory fulfillment of train-cars are carried out at each yard/tail track. Rather than breaking a
10-car consist arriving to the yard to send out a 5-car consist, the 10-car consist goes to inventory
while a 5-car consist is sent out from inventory, if available. This avoids unnecessary making and
breaking costs.


## Data 

- alpha.pkl
  - Train schedule departure times. 
  
- beta.pkl
  - Train schedule arrival times. 
  
 - intervals - intervals.csv
   - Train line data. Time to travel, miles between stations. 
   
 - all_yards_indexes  all_yards_indexes.csv
   - Yard inventory data
   
 - passenger_flow - passenger.csv
   - Passenger demand data. Week day by hour. Number of passengers. 

### Pre-Processing NoteBooks

- PreProcessData_v3.ipynb
  - Generate departure and arrival times from raw BART schedule data. PreProcess inventory yard event table. Generate data structures. 

## Presentation

See presentation directory. 

## Report 

See report directory. 


