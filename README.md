# Lead Score conversion - Sales and Marketing

## Business Understanding :
</br>
Analysis was done for edtech platform which sells online courses to industry professionals. The company markets its courses on several websites and search engines like Google.  On any given day, many professionals who are interested in the courses land on their website and browse for courses.
Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form
providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads
through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc.
Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is
around 30%.
Now, although Edtech platform gets more leads, its lead conversion rate is very poor. To make this process more efficient, the
company wishes to identify the most potential leads, also known as ‘Hot Leads’.
The company requires you to build a model wherein need to assign a lead score to each of the leads such that the customers
with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion
chance. The bench mark of the target lead conversion rate to be around 80%.
</br>
## Dataset and Steps overview :
</br>
The dataset consists the basic info about these potential leads such as how they come to know about the course, how much time did 
they spend on the website, also how many time did they visited the website so on. </br> 
Following is the approach that we used in this problem :
</br>
1.Data Cleaning:
The dataset consist of various missing values and ‘select’ as one of the value which needed to 
be replaced as it was not providing any info. The “select’ value was replaced by Nan value and 
the columns having missing or null values more than 45% were directly removed. The rest of 
the missing values were either imputed with the mode value or with “not specified” value. 
Columns having very minimal missing values were removed alongside the rows, reducing the 
total number of rows in the dataset. Other than this few column had dominating single values 
such as countries column had India as a value around 98% so this column was removed as it 
was causing imbalances, similarly few other columns were also removed. Column “Lead Origin” 
contains value as Google with “G” and “google” wioth “g” so the google was replaced by 
“Google”.
</br>
2. Exploratory Data Analysis:
In EDA part we analysed few numerical columns and found out they had few outliers, these 
outliers were treated by removing the top and bottom 1 percentiles of value.
</br>
3. Dummy variables:
All the categorical columns were assigned dummy variables and the original column was 
removed. For numerical values standard scaling was performed.
</br>
4. Train Test Split.
The dataset was divided into 80:20 ratio for train and test purpose and make predictions based on the accuracy of model.
</br>
5. Model Building:
Using the RFE model 15 features were identified. Later based on the p value and the Variance 
Inflation factor few columns were dropped. The value of p value was kept below <0.05 and VIF< 
</br>
6. Model Evaluation:
For predicting the model accuracy confusion matrix was used and the accuracy for training and 
testing set was found out to be nearly 92%.
</br>
8. Recall :
The recall value for the model was approx 91% with 89% precision.
</br>
Top three variables in your model which contribute most towards the probability of a lead 
getting converted are :
a. 'Total Time Spent on Website'
b.  ‘Last_notable_activity_sms_sent’
c.  'Tags_will revert after reading the email' </br>
</br>
Good strategy they should employ at this stage. </br>
1. Make phone calls to the leads having lead score of greater than 60. </br>
2. Make phone calls to the people spending more time on website and are currently 
working professionals. </br>
3. Few Interns should be dedicated to make the website more engaging and user 
friendly </br>
4. Leads with Last activity as SMS sent should be followed up regularly as they have high 
chance of being converted. </br>
.
