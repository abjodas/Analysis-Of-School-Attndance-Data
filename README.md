# Analysis-Of-School-Attndance-Data
I have taken a dataset from Kaggle which contains attendance data for all the schools in New York City

## Let Us Start By Trying To Understand Our Dataset

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/97d4bd18-81bf-4824-96af-8d4ebafd2a3b)

We can see that our data contains School DBN which is an unique identification number given to every school in NYC. We can also see a Date column which has the yearmonthday format, enrolled, absent and present columns.

#### It will be better of we properly format the date. So, let us do that
![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/8f69c890-4c52-4dad-8c0a-f2f39960a2b6)

Now lets analyse the data

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/d47ab41e-ffa1-4587-82cd-bee490fa5c77)


We can see that there has been a day when 2151 students were absent. The median is 38 which means 50% of the data has absentees as 38 or lower, which is not bad. But, I think we will get a better picture if we calculate the absentee rate and then visualize that.

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/98b2aa44-406b-404b-8e45-726aad41c018)

We can see that on average, the absentee rate was about 10%. We can also see that the median is 7% and 75% of the data is within 11.6%. Also, the maximum absentee rate is 99.6%, this means that there are outliers.
![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/3e10b142-a6a2-4840-a50e-69f793fbc94f)

We can see that the right whisker is longer indicating a skew to the right. We can also see many outliers indicating the days when the absentee rate was exceptionally high.

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/4857fb2b-92fb-4211-a0dc-82f8c4dcb7da)

We can see that the average monthly absentee rate is highest in June. One possible explanation of this might be that many schools hold exams this month and the students prepare for these exams by staying home and missing a few classes. The final classes often include revisions and perhaps the students feel that they can revise better at home by dedicating their time focusing on their weak subjects.

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/ac5c161b-82ec-464b-8fce-6a7f250293e5)

We can see that some schools have exceptionally high absentee rates. We can also see that some schools have almost 0% absentee rates. This means that some schools are better than the others at managing their absentee rates.
![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/8b673110-51b7-47d6-afbc-e738512dcc6e)

We can see that on average, students miss their classes most on Fridays. This can be because missing the class on Friday gives them an extra day of holiday after including the weekend.

### Adding weather data for each date can help us find a correlation between the weather and absentee rates

So, I scraped wunderground.com for historical NYC data and aggregrated that into the dataset. I will try to get individual weather data for each district mentioned in the school dbn in a future update. For example, M stands for Manhattan. 

![image](https://github.com/abjodas/Analysis-Of-School-Attndance-Data/assets/47302962/c9b6bd55-96f3-4533-8fd0-95c0615dcbcc)

We can see that absentee rates are exceptionally high when the temperature is around 16-20 Fahrenheit or -9 to -6 Deg Celsius. The most obvious explanation is that students do not prefer to attend classes when it snowing or it has snowed. They prefer a more pleasant climate. We can see the absentee rate rise from about 81-90 Fahrenheit. This means that they do not prefer to attend classes when it is very hot.

I have added precipitation data as well, but the results were inconclusive, perhaps due to the fact that getting precipitation data for each district is much more necessary than temperature. Also, the timing matters. If it rains at night or after the school has started, it will not affect absentee rates in the slightest.




