# Hypoglycemia_Detection_MA

This thesis aimed to classify the onset of hypoglycemia up to 24 hours before while including 9 prediction horizons. The classification performances of a ResNet, an LSTM, and a ResNet+LSTM model were compared. 

- Data_Read_Preprocess: reads the wanted columns from the xml files, resamples every feature to 5 minute intervals, and applies linear interpolation. Then big gaps are removed and the dataframes split into multiple subdataframes without any gaps, and finally each subjects's data is saved as csv files.

- Correlation_Analysis: correlation analysis (individual and population based) and population-based pair-wise plots between glucose, basal inuslin, bolus insulin, and magnitude of acceleration

- Visualization: plots the values of glucose, basal inuslin, bolus insulin, and magnitude of acceleration for the last 48 hours before hypogylcemia for each subject

- LOOCV_ResNet_LSTM: Compares the ResNet, LSTM, and hybrid models for 9 classes and 6 classes which classifies up to 4 hours before hypogylcemia. Moreover, each trained model is further trained with 50% of the data of the test person

-  LOOCV_ResNet_LSTM_less_test: To enable a comparison between subjcet-specific and population-based models, the trained models are tested with the same 30% of the test person like the subject-specific models 