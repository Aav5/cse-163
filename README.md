# cse-163
Project in Data Programming
Study of Covid-19 Patterns: with Data visualization and ML
By Aniruddh Vardhan
Summary of questions and results

1.	For my first research question I was curious about how has vaccination rates for covid-19 vaccines for the world population changed over time and what could be possible future trends? Also, how are vaccination rates in different regions of the globe?

From my findings I could see that covid vaccination rates have taken great pace after January, 2021 for most of the world and has been rising ever since. I would say it would continue to rise as we move forward.  However, I also found out that the distribution of covid vaccine rates has not been regular across different continents. 

2.	Is there a co-relation between GDP of a nation to factors like vaccination rate? If yes, Is GDP of a nation sole factor determining the co-relation?

Yes, there is absolutely a co-relation between GDP of a nation to factors like vaccination rate with the high GDP nations having higher vaccination rate and vice versa. I found that GDP of a nation is not sole factor determining the co-relation, the continent a country is in also impacts vaccination rates

3.	How does having a pre-existing diseases like cardiovascular /heart disease affect one’s chances of survival after contracting covid-19?  
In my conclusion, I found out that a pre-existing cardiovascular /heart diseases makes one’s chance to survive to about a half.

Motivation
As covid is spreading and the world stays unclear of the future, understanding covid trends till now and having a projection of future covid rates would help us give an idea about resources we need to keep prepared to make sure all basic goods are able to be delivered/provided to general public and in large what to expect the future in this time of uncertainty.
I was also curious about seeing how vaccination rates or access to vaccines changes according to country’s location or GDP as there have been many questions about relationship to wealth and the infections rate relation and also the relationship of wealth to the protection to covid-19 i.e. vaccination rate.
Lastly, as there is yet more research to be done with how covid-19 affects people who already are sick. As cardiovascular diseases are world’s one of the biggest cause of death and knowing that covid-19 affects internal organs till certain degree, I was interested to learn how an existing medical condition like cardiovascular diseases would affect a persons chance of surving after contracting covid-19 This would help us to understand the risks what existing medical condition could have along with having covid-19, and understanding this would help us be more prepared for future times.
 
Dataset
https://www.kaggle.com/georgesaavedra/covid19-dataset
From the above link I took a covid-19 dataset in a csv file format. The data sets has information about covid-19 positive cases, deaths, vaccinated people and so on of all countries around the world.
https://www.efrainmaps.es/english-version/free-downloads/world/
From the above link I used a shapefile including data about world international borders.
Methods & Results
1- For answering the 1st research question, I decided to make a line plot of total vaccinations per hundred over time. For doing this I first added the needed packages and files to my python file. Then I read the dataset with code. After which, I cleaned the data according to my needs by using date column from the csv file and changing format to use it. Then, selected regions in much I was to want to result of total vaccination per hundred in that particular region. I decided to choose continent as regions. After, pricking all the data I needed from the dataset, I plot a line plot of total vaccinations per hundred over time using seaborn, and give me labels, tittles, and legend using matplotlib, to make my line plot understandable. 
This line plot helps us to see how after January 2021 there a spike of rate of vaccinated people was. Which continues to increase almost exponentially as time passes by. Looking at current state the vaccination would only been on increasing. Another thing to notice in this plot was that how vaccination rates in African subcontinent started increasing rapidly only after months after other continents And was and continues to remain the lowest among all habited continents, even below the world average vaccination rate.
 
2- Moving forward with what I learnt from this plot and considering my next research question, I decided to go deeper on how unequal the distribution of vaccinations rates have been across the globe. So, for my 2nd research question I used the previous plot teachings and a choropleth world map with world’s country GDP. To start with I used the same previous csv data, which also includes GDP of every country in the dataset. I also used another dataset which includes of a shapefile of the world map spited with countries across the globe. I started off with loading data and carefully observing and understanding it. I then cleaned the data and joined csv and shapefile together with a merge operation at the columns 'SOVEREIGNT' and 'location'. I used this joint dataset to plot a choropleth world map with world’s country GDP using seaborn. After that I added tittle, and legend to the map using matplotlib. This gave me a visualization of how there was a correlation between the distribution of global wealth and vaccination rates. The factors which would be easily noticed would be the GDP of an income and also the continent a country is located in. There was a higher vaccination rate in richer countries and specially ones in North America, Europe, and Oceania. On the other hand, many countries in Africa and other countries with lower GDP in Asia and South America have a lower rate of vaccination.
 
 
3- Lastly, for 3rd research question I decided to make a machine learning algorithm to determine the likelihood of a person with heart condition to survive after contracting covid-19. For doing so I heavily used the library sklearn. I started with taking in data from the csv file. Which was later cleaned and only only needed data I took from the original csv file. I applied dropna() function to drop all NaN values in my process of cleaning the data. Then I set features and labels of the Machine Learning algorithm. Features include all selected columns except ‘continent’ column and labels is the continents column. I then set my dataset to train with a smaller set of selected sample data and use DecisionTreeClassifier with max_depth=3 to form the model. The model is then trained and result of it is presented. My result came up to be around 0.5. Which suggests that people with cardiovascular problems are at great danger to contracting covid-19. 
Impact and Limitations 
From my result we can see that covid-19 vaccination rates are yet rising. Hwoever, not all population is able to benefit from it. It is unequal to people of poor nations and thus the pandemic would continue to exit. 
From my analysis the government could use the data, supply chain managers and retailers could use the data to understand how to operate their business, hospitals and schools too can benefit from my data. I don’t see any potential harmed party from my data. There could be a bias for my 3rd research question answer, as it is not clear in the data how severe the heart conditions and different results are could come with changes to that information. A limitation for my analysis could be that my machine learning algorithm does not include several important factors like age to conclude the chance of survival of a person with heart condition. 
Challenge Goals
One of the challenging goals was working with a large dataset. I tried working of edstem. 1st but my plots kept on crashing. Only after meeting a TA, I decided that I would rather solve it in local computer.
Another issue I faced was not being able to print/plot things instantly like we did in jypyter. Even though it was suggested for testing, I though that running large datasets on different places on a single computer screen to be not the best way and thus had to make several errors before making my graph. 
Lastly, Ploting my gdp map was a problem as the shp file and csv file had different names for certain country. Eg America, USA.

![image](https://user-images.githubusercontent.com/59792797/160266095-2d290f71-4927-494e-8b97-93a56bbaa474.png)
