# Hypoglycemia_Detection_MA

- Data_Read_preprocess: reads the wanted columns from the xml files, resamples every feature to 5 minute intervals, and applies linear interpolation. Then big gaps are removed and the dataframes split into multiple subdataframes without any gaps, and finally each subjects's data is saved as csv files.

- Data_Analysis: Correlation (individual and population based) and Plot of Features during Hypoglycemic events (individual based)
