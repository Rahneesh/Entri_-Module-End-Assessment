# Entri_-Module-End-Assessment
============================= Date Base: US car market =====================================================================
Features explanation
1. car_ID
- Unique identification number for each car
- No meaning in prediction, just for indexing the number of cars. Not useful for data analysis
2. symboling
- Car risk/safety rating
- Range: –3 (safe) to +3 (risky)
- Insurance-based safety score
- High safety score means high safety and high price
3. CarName
- Brand + model name of the car
- Contains spelling mistakes 
- Brand value also needs to be checked here. So, car name and varient needs to be divided into two different feature. 
4. fueltype
- Type of fuel
- Values: gas, diesel
5. aspiration
- Type of air induction
- Values: std, turbo
- Turbo increases power
6. doornumber
- Total number of doors
- Values: two, four
7. carbody
- Body style of the vehicle
- sedan, hatchback, wagon, convertible, hardtop
8. drivewheel
- Which wheels drive the car
- fwd = front wheel drive
- rwd = rear wheel drive
- 4wd = four-wheel drive
9. enginelocation
- Where the engine is placed
- Values: front, rear
10. wheelbase
- Distance between front & rear wheels
11. carlength
- Total length of the car
- Longer cars often = more interior space and high cost
12. carwidth
- Total width of the car
13. carheight
- Total height of the car
14. curbweight
- Weight of car without passengers
- Heavier cars usually consume more fuel
15. enginetype
- Type/design of engine
- dohc, ohc, ohcf, l, rotor, etc.
16. cylindernumber
- Number of cylinders
- More cylinders = more power
17. enginesize
- Engine displacement (cc)
- One of the strongest predictors of price
18. fuelsystem
- Fuel delivery method
- mpfi, spdi, carburetor, idi, etc.
19. boreratio
- Cylinder bore diameter
- Higher bore = more power potential
20. stroke
- Piston travel distance
- Paired with bore → defines engine design
21. compressionratio
- Pressure level inside cylinder
- Higher ratio = more efficiency
22. horsepower
- Engine power output
- High horsepower means more power to the vehicle and it leads to higher price
23. peakrpm
- RPM at which maximum horsepower is produced (or simply maximum speed)
24. citympg
- Fuel efficiency in city conditions or high traffic area
25. highwaympg
- Fuel efficiency on highways
- Usually higher than citympg
26. price
- Target variable
- Selling price of the car (USD)

=================== Aim ===================================================
To give bussiness insight to a chinease manufacturing company about US car market

=================== Preprocessing ==========================================
- No Null Values
- Duplicate car values and spelling mistake removed
- Luxury car brands classified seperately
- Number mapping for car door number, engine cylinder number, etc
- One hot encoding for categorical values
- Distrbution curves for the numerical values
- Outlier values are observed, but decided not to remove as those are for luxury cars

====================== Model ================================================
- Tried different regressio models like linear regression, decision tree, RF, GBR and SVR.
- Gradient boost gave the best result due to its boosting character
- Hyperparameter tuning done for GBR
- Importance of the features identified

======================= Major factor affecting the price ====================
Major features which change the price are as follows
- Engine size
- highway mileage
- curbweight
- horsepower
- Luxurycar or not
- carwidth
- Wheelbase

======================== Verdicts ==========================================
Insights for Designing a Car Model (Based on ML Price Analysis)
1. Engine Size (enginesize)
- Price increases sharply with engine size.
- Affordable cars should ideally keep enginesize ≤ 200 units.
- Higher enginesize pushes the model toward the premium/luxury segment.

2. Highway Mileage (highwaympg)
- Shows a strong negative relationship with price.
- Affordable cars should aim for ≥ 30 mpg highway mileage to attract cost-conscious buyers.

3. Curb Weight (curbweight)
- Curb weight increases price, but the effect becomes less sharp between 1500–2500 units, where cost differences are minimal.
- Using an optimal lightweight design can help control price without major performance sacrifice.

4. Horsepower
- Price rises noticeably after ~100 HP.
- Affordable performance-focused cars should target 90–100 HP, balancing power and cost.

5. Car Width (carwidth)
- Strong positive correlation with price.
- Most affordable cars fall within 60–68 units.
- Wider cars (>68) generally move into the luxury category due to design, features, and segment positioning.

6. City Mileage (citympg)
- Shows a similar inverse trend as highway mileage.
- Even luxury cars maintain ~20 mpg, suggesting efficiency expectations across segments.

7. Car Length (carlength)
- Affordable cars cluster around ~190 units.
- Models longer than this generally belong to the luxury category due to additional cabin space and premium design.
