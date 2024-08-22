The dataset is provided by https://git.embl.de/varik

It is python implementation of 4PLregress model implemented here
https://git.embl.de/varik/32drugs/-/tree/master

Only data taken from above repository is (01_dat.csv, 02_dat_csv, 03_dat.csv)



For first time setup after installing python, download the requirements.txt file 
go to cmd/Annaconda prompt and run the following command
pip install -r pip install -r "PATH\TO\requirements.txt"



There are two jupyter notebooks, first one is for data preprocessing and second one is for model building

# 0_Data_preprocessing
## 0.1. Data Loading
* Read all the csv files from data directory and create dataframe
* Remove duplicate/identical rows from the dataframe, since the data was incremental (consisting from previous days in the newer csv files)
* Plot the visualisations for all three days
## 0.2. Feature Engineering
* To construct the model we need to create OD and Fit columns
* Add OD column
* Change all values in OD column to 0.03 where the row.OD < 0.03
* Add Fit Column
* Change all values in Fit column to 1.1 where the row.Fit > 1.1
## 0.3. Export the results
* export the complete csv to result directory
* export the filtered result for Time_h between 9.5 < Time_h < 10.5 and uM !=0


# 1. Model_building
## 1.1. Data loading
* read the filtered result csv from result directory and create dataframe, uM is independent variable and Fit is dependent variable
## 1.2. Model Assumptions
* If it follows s-curve and have monotocity
## 1.3. Model Construction
* construct the model
* visualize the trend line using linspcae and logspace
## 1.4. Model Validation
* Validate the model
* Calculate R-square values
* Calculate MSE
* Calculate Confidence interval of the parameters
## 1.5. Model predictions
* run dummy data on it






