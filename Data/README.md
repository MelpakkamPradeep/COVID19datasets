### **WHO-COVID-19-global-data.csv** ##
This dataset was obtained from the WHO website (https://covid19.who.int/WHO-COVID-19-global-data.csv). The new cases data till 20th October 2021 was used to generate the images in the "Results/Images (Cases)" directory. The new cases data till 27th May 2022 was used to train and test all models, and generate all other datasets.
### **COVID19_Dataset_v1.csv** ###
Contains only the new cases data (from the WHO dataset), along with the country code, date of reporting and whether the day is part of a wave (1) or not (0).
### **COVID19_Dataset_v2.csv** ###
Contains a list of the new cases data of all days part of a "wave" as per the predicting algoirthm. Along with this, the country code, date of reporting and whether the stretch (i.e., list of new cases) is part of a wave (1) or not (0).
### **COVID19_Dataset_v3.csv** ###
The column "T21" refers to the new cases data corresponding to the date present in the "Date_reported" column. The columns "T1" to "T20" contain the new cases data for the 20 days prior to the date corresponding to "T21". The columns "Residual", "Seasonal" and "Trend" contain the components of the decomposed new cases time series. The packages and codes used for this can be found in the "Codes" repository, in the file "COWAVE.py". Along with these columns, the country code, date of reporting, and wave label are also present in the corresponding columns.
### **COWAVE.csv** ###
Contains the complete dataset generated in this project. All features present as columns have been explained in detail, in the accompanying paper. This dataset was generated using the file "COWAVE_gen.py", present in the "Codes/" directory.
