# Breast Cancer Detection
<br><br>

# My NoteBook will be divided into 2 main parts which are
 - Data Analysis and Cleaning part
 - The Machine Learning Model 

<br><br><br>

## First : Data Analysis and Cleaning part :
>  - First: Importing data and making dataframe column names
>  - Second: Data exploration
>  - Third: Data cleaning and replacing NaN values
>  - Fourth: Making sure that data is fully clean and with no duplicates or NaN values

<br>

##### First : I did is to load "breast-cancer-wisconsin.data" from "Datasets" folder but there was no header column so I got header column using "breast-cancer-wisconsin.names".  <br>
##### Second : So my dataframe is ready for exploration stage, where I checked data shape and info and searched for duplicates and I noticed many thing which is :<br>
 > - Some Data types are not correct <br>
 > - I got complete 8 duplicates and after removing these duplicates I got another 46 id duplicates (I considered  them an errors in entering data which needs to be removed !!)
 > - datatype of "Sample code number:(id number)" and "Class:(2 for benign, 4 for malignant)" columns is int (So I need to change it to object)
 > - In column "Bare Nuclei:(1-10)" I got missing data in the form of "?" string 
 <br>
 
 ##### Third : Now I need to change datatype of "Sample code number:(id number)" and "Class:(2 for benign, 4 for malignant)" columns to be object instead of int, and I need to replace NaN values in "Bare Nuclei:(1-10)"<br> Changing columns datatype was easy but while replacing NaN values in "Bare Nuclei:(1-10)" column I needed to learn what is the reason of being a Bare Nuclei and how to replace NaN values based on other columns (using heatmap to see the correlations)
 
 ##### Fourth: Now I will check data again to see if it is ready for using it to train the ML model so I checked info and dtypes and NaN values and I removed id column, and the results was very satisfying, So this was the end Data analysis part.
 
 <br><br>
 
 ## Second : The Machine Learning Model :
>  - First: Training the model
>  - Second: Measuring the accuracy
>  - Third: Choosing the model parameters
>  - Fourth: Ensuring my results by manually testing my data on the model ,and see the outputs


##### First : I trained the model using KNN Classification Algorithm and I splited data so that 30% testing data and 70% training data<br>
##### Second : I want to choose best k with highest accuracy so I made a loop to see best k with best accuracy for training and testing and I graphed the relationship between them<br>
##### Third : The best model accuracy was at K = 1 it nearly got 100% accuracy which is spectacular, The model at k = 1 is perfect rather than other k values
##### Fourth : To see the results by myself I manually entered the last 200 row in my data to see how will the model give the results <br> After doing so I got 199 from 200 correct outcomes and 1 from 200 wrong outcome... So that was very satisfying.

### So at the end I made the model with K=1 and the model is ready based on the data I got
