# Bellabeatღ Case Study
Case Study performed for the hypothetical Marketing Analytics Team of Bellabeat.

Bellabeat is a high-tech company that manufactures health-focused smart products. Their mission is to empower women with knowledge about their own health and habits by collecting data on activity, sleep, stress and reproductive health.

The marketing analytics team wants to focus on a Bellabeat product and analyze smart device usage data in order to gain insight into how people are already using their smart devices. This way, recommendations would be informed for Bellabeat’s marketing strategy.

Key questions for the analysis:

##### · What are some trends in smart device usage?
##### · How could these trends apply to Bellabeat customers?
##### · How could these trends help influence Bellabeat marketing strategy?

### Preparing the data

Kaggle is an online community platform for data scientist’s. It contains numerous open datasets to be explored. A particular dataset will be used in this analysis; FitBit Fitness Tracker Data by Möbius.

The dataset contains multiple csv files that will be opened in spreadsheets; dailyActivity_merged, sleepDay_merged and weightLogInfo_merged will contain the most relevant information for the understanding of the user’s behaviour.

Quick Summary: These files collect records of the different users every day for a duration of one month. From the 12th of April 2016 to the 12th of May 2016, considering that some users do not present the data for the entirity of the month.

Through each record, new information is proposed in various topics like; Total Steps, Total Distance, Calories Burned, Total Time in Bed..etc that will help in terms of the interpretation and contextual understanding of Fitbit Users.

### Processing the data

The tool to be used will be Google Sheets, a spreadsheet program containing various options for cleaning and sorting the data.

Finally after some adjustments, a single csv file is ready: Download File. It contains all the values to be worked with that are organized and validated.

!When downloading the file, the name should end with “.csv” so that the system can detect that it is a comma-separated values file.

##### · The first five columns and rows of the data:

<img width="604" alt="image" src="https://user-images.githubusercontent.com/92883393/177405305-96583495-d4c2-487b-b018-8ad9470ba08b.png">

##### · The first rows from the documentation of the cleaning process, the entire file can be located in the Input Section below:

<img width="608" alt="image" src="https://user-images.githubusercontent.com/92883393/177405436-436eb18a-1e04-4990-ac35-12725d9e315b.png">

### The Analysis

The analysis phase will help in terms of identifying the most noticeable aspects of the data as well as figuring out what relationships the values in the dataset hold with each other.

Arguably the most notable feature upon looking at the dataset is the amount of zero values the column Logged_Activities_Distance contains.

##### · The values in the column that are equivalent to zero by boolean terms:

<img width="608" alt="image" src="https://user-images.githubusercontent.com/92883393/177405655-04f245b1-a919-4fc1-abb1-0dfdd5bb75b9.png">

##### · The percentage of zero values:

<img width="608" alt="image" src="https://user-images.githubusercontent.com/92883393/177405732-eab11aa1-e433-4c30-8ab8-4023dc808481.png">

*This goes to show that the users have shown very little interest in terms of logging in to track their distance.*

RStudio can help gather some data insights through it’s visualization capabilities, also considering how effective the tool is. Here are some explorations:

#### 1- The Average Total Steps Per Day

<img width="500" alt="image" src="https://user-images.githubusercontent.com/92883393/177406436-6b515c2d-b032-4ef2-91d5-5bcdbd8ae84e.png">

*The trend line seems to be somewhat stable throughout the days, while the most noticeable change comes out to be in the end where there seems to be quite a significant decrease in the steps.*

#### 2- Total Distance (km) vs Total Steps

<img width="504" alt="image" src="https://user-images.githubusercontent.com/92883393/177406571-fa6b067a-7477-4493-88f7-92cba0d44894.png">

*The scatter chart demonstrates that there is a positive correlation between the two variables. Meaning that as the total steps increase, so does the distance, which is a logical validation.*

#### 3- Percentages of Active Distance

<img width="473" alt="image" src="https://user-images.githubusercontent.com/92883393/177410157-55882ef2-db7b-4ca8-9652-6cce42b89e9b.png">

*The values shown make up the Total Distance (km). The most prominent category is Light Active, therefore revealing that the users have covered the most distance lightly active. Sedentary Active presents itself the least, signifying that users do not cover notable distances while sedentary/inactive on average, as expected.*

#### 4- Percentages of Active Minutes

<img width="449" alt="image" src="https://user-images.githubusercontent.com/92883393/177407024-05ef8829-41ff-46b4-896d-c00348a793f5.png">

*Percentage values from minutes recorded from the entire day, on average. Sedentary minutes seem heavily distinguished from the rest, given that most users have spent their time inactive throughout the whole day and aproximately 20% of the day is spent in some active form.*

#### 5- Calories vs Total Steps

<img width="502" alt="image" src="https://user-images.githubusercontent.com/92883393/177407128-567cc3ff-b528-41b1-85c1-5299a4970ec6.png">

*The Calories values share some relationship with the Total Steps, one where there seems to be a similar behaviour between both, considering that the Total Steps values come out to be much more exagerated in comparance.*

#### 6- Percentages of Total Time in Bed & Nº Sleep Records

<img width="401" alt="image" src="https://user-images.githubusercontent.com/92883393/177409784-b80ec807-7db4-42e2-a462-c04eac184302.png">

<img width="404" alt="image" src="https://user-images.githubusercontent.com/92883393/177409885-767573e1-095c-475d-9047-91b51eef7546.png">

*The pie chart of the top shows that out of all the Total Time in Bed (minutes), 91.3% of that time was measured as the user being asleep, whereas 8.75% of that total time, the user was not asleep.*

*In the bottom chart, Total Number of Sleep Records has been collected. It shows that approximately half of the values are Null (meaning no answer), while the rest is composed between 1-3 sleep records.*

#### 7- BMI & Weight

<img width="479" alt="image" src="https://user-images.githubusercontent.com/92883393/177407509-f51af5e7-476a-41b8-9c42-d271edec88c6.png">

<img width="500" alt="image" src="https://user-images.githubusercontent.com/92883393/177407564-b48949d6-9116-4753-9cbb-1ad15333b584.png">

*The upper chart shows how much load Null values have in the variables. Therefore demonstrating that BMI and Weight Reports are not predominantly considered by the Users, which indicates minimal interest.*

*The lower chart is quite localized, due to the fact that the User Nº25 was the only user to record their Weight and BMI every day (leaving one) for the entirity of the month. As per the visualization, the trend seems to have been stable, not indicating a significant loss or gain in Weight &/or BMI.*

#### 8- Manual Report Percentages

<img width="431" alt="image" src="https://user-images.githubusercontent.com/92883393/177407671-ea19ddbc-5540-4832-8393-a93276e0dee9.png">

*In this pie chart, the indication is that around 95% of Manual Reports values are Null. As this variable is related to the BMI variable. It reveals that only for the records (values that are numeric & not Null) in BMI, the Manual Report is either True or False, where True is held more accountable.*

#### 9- Total Hours Asleep

<img width="496" alt="image" src="https://user-images.githubusercontent.com/92883393/177407756-2134f25b-13e3-4325-8679-94e283b4142e.png">

*Last but not least, this histogram implies on the total hours slept by the users given the records.*

### Sharing The Findings

Key findings to take into account after the analysis:

* 1- Total steps taken every day vary and does not seem to illustrate a steady trend. Furthermore, if a peak in steps is to be noticed on a specific day, the next day would equate to the user performing less than average steps. Representing a “wavy” trend.

* 2- Users have shown to cover most of their distances (km) lightly active. Meaning that a steady walk would be what people would tend to perform the most when covering distances. Further equating to that LISS (Low-Intensity Steady State) Cardio would be quite beneficial in terms of burning calories compared to HIIT (High-Intensity Interval Training) Cardio, as most of the distance and time is covered in “Lightly Active”.
      A good demonstration will be the Exercise Calories Burned Calculator:
      
Activity in Minutes x (MET x 3.5 x Weight(kg)) / 200 = Calories Burned

Activity in Min. = Considering the mean of the “Light & Very Active Minutes” columns amongst all users.

MET = Type of Exercise (Every Exercise has its own numeric value)

Weight = 70kg (A Weight to consider for the calculation)

<img width="589" alt="image" src="https://user-images.githubusercontent.com/92883393/177408542-bf788a7c-e4cf-4f85-919e-1b2ccc53a697.png">

<img width="590" alt="image" src="https://user-images.githubusercontent.com/92883393/177408594-bd94081d-c76c-46a5-94c0-3156f78834ca.png">

<img width="590" alt="image" src="https://user-images.githubusercontent.com/92883393/177408709-3a8a5fe2-8d6b-4c64-bc87-5b9b3871351b.png">

These values show of how much one approximately (on average) burns through being Lightly Active (ex.LISS) than to being Very Active (ex.HIIT) in the entirity of the day. There is a significant difference:

**1204.937 calories in Lightly Active**

**454.9988 calories in Very Active**

In conclusion, most of people’s activities consists of **LISS** , this is due to the fact that apart from working out, people also do other types of light activities throughout the day like shopping, taking a walk, playing sports, going to work..etc

Naturally if you did **HIIT** on a specific day, you would feel tired the entire day because of how you had exhausted your body with such vigurous activity. Meaning you would spend more time laying back on the sofa or taking a nap, therefore being more sedentary and not losing significant calories.

With **LISS** , you have not exhausted your body to a point where it has no energy, so you would tend to do more activities.

* 3- Users don’t bother with having to log in to record their distance covered, as shown in the analysis, out of all the records from the users, 96.23% have no record (meaning 0 km).

* 4- The amount of calories burned is not significantly impacted by the total steps covered during the day. Demonstrating that there is no strong correlation between both variables.

* 5- BMI & Weight Reports are also, in the majority, not considered by the users. Only a few values have been reported out of all the days of each user. The reason might be associated to the fact that users are not using their Fitbit predominantly for weight loss. Excluding one user (#25), who has shown that the weight and BMI trend was stable, with no significant change, in the entirity of the month.

Out of all the BMI & Weight records, around 96% were manually reported.

### Final Act

Upon the findings:

* It would be best to establish to the user, what goals they’d want to achieve by using Bellabeat’s smart devices. Some users would show appreciation towards “Health”, while others might be more inclined towards “Weight Loss”. There is a significant difference, as users going after “Weight Loss” would emphasize in making reports on their Weight and BMI. Whereas those heading for “Health” would put special attention on reports of their Sleep Activity.

* LISS Cardio would be an ideal suggestion to those who preach “Weight Loss”, as it makes a significant difference upon burning more calories throughout the entire day.

* Logging in is an attribute hardly any use in terms of recording their distance. A better solution would be to not have the users have their credentials manually put in and instead have an “Automatic LogIn” option, if that was not already the case.

* Special emphasis should be put in terms of additionally automating the BMI & Weight reports, as conceivably, because the users noticed that reports had to be manually stated. It’s usability decreased, hence the predominant null values in this analysis.

* As seen in the graph of the analysis section, a significant portion of the users have spent their total hours of time sleeping less than 6 hours, which is not ideal for the majority. It is highly advisable to reiterate that adequate sleep is essential, as it leads to a healthy body and mind.

*The National Sleep Foundation guidelines advise that healthy adults need between 7 and 9 hours of sleep per night.*

**These are some recommendations based on the findings, thank you for your time!**






