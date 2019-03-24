Udacity - Data Analyst Nanodegree
Name : Ahmad Abu Saida
Project 1 : Exploring Weather Trends
Introduction :
Global Warming had risen the topic of discussing about the current temperature trends and analysis is being performed to analyses the temperature increments. In this publication, global temperature’s are analyzed with respect to local temperatures to determine whether or not temperatures are climbing over time.
Local and global temperatures are analyzed and compare the local temperature trends with global temperature trends.
Method :
The data that was being used in this analysis are being retrieved from database using Structured Query Language and then analysed using Excel spreadsheet. The data was analyzed using 10 year Moving Average to make trends more clear.
Data from Database : Retrieving
Data was retrieved from the database using SQL - Structured Query Language. Visualizing data to assure that we are going to retrieve the actual data that we should perform analysis from various data available in multiple tables in the database.
- To see the available nearby city whose temperature data is available : SELECT * FROM city_list WHERE country = 'Saudi_Arabia';
- To visualize the local city_data SELECT * FROM city_data WHERE city = 'Riyadh' AND country = 'Saudi_Arabia' LIMIT 10;
- To visualize the global_data SELECT * FROM global_data;
- To retrieve the final data from database from multiple tables
ALTER TABLE city_data RENAME COLUMN avg_temp to local_avg_temp; ALTER TABLE global_data RENAME COLUMN avg_temp to global_avg_temp;
SELECT global_data.year,city_data.city,global_data.avg_temp, city_data.avg_temp
FROM global_data,city_data
WHERE(global_data.year = city_data.year) AND (city_data.city = 'Riyadh' AND city_data.country = 'Saudi Arabia');
- Download the .csv file and open it in Excel Spreadsheets.
- Moving Average’s for 10 years are calculated for global_avg_temp and local_avg_temp to smooth out data and make it easier to observe long term trends after plotting the line chart. - Line chart’s are plotted using spreadsheets inbuilt features for Global temperatures versus Local temperatures with respect to year.
Results and Discussions
Figure 1: Before Moving Average’s Average temperature in celsius over time in years with Global values in Red and Riyadh in blue.
It was found that average global temperature is increasing over time. Global temperature trends were depicted in red where as Riyadh temperature were depicted in blue. From 1915 the average global temperature was increasing . Riyadh average temperature was slightly high when compared to global temperature because global temperature includes various such parameter’s unlike Riyadh trends. For smoother and clear analyzing the longer trends we will transform the line chart into Moving Average’s Line chart.
0
5
10
15
20
25
30
TemperatureTemperatureTemperatureTemperatureTemperatureTemperatureTemperatureTemperature
YearsYearsYears Years
Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global
local_avg_templocal_avg_templocal_avg_templocal_avg_temp local_avg_templocal_avg_temp local_avg_temp local_avg_temp
global_avg_tempglobal_avg_tempglobal_avg_tempglobal_avg_tempglobal_avg_temp global_avg_tempglobal_avg_temp global_avg_temp global_avg_temp
Moving Average 10 Years
Figure 2: Average temperature in celsius over time in years with Global values in red and Riyadh in blue in Moving Averages for 10 Years.
The temperature trends of Riyadh are quietly high when compared with global temperatures. In 1933 the moving average of Riyadh is 25.21 whereas for global it is 8.66. This clearly depicts that the average temperature’s of Riyadh are higher than the global average temperature’s.
Riyadh temperature trends slightly increase from 1987 to 2013. Global temperature trends are also similar to local temperature trends in terms of increase. It maintains consistent in nature with small increases in temperature trends.
The curve’s of Riyadh temperature trends maintain’s higher variance when compared to global through out the line chart. Hence, we can conclude that "Riyadh is hotter when compared to global average”.
- The difference between the Moving Average temperature trends of Riyadh and global in 1843 is : 23.07 – 8.05 = 15.03
- The difference between the Moving Average temperature trends of Riyadh and global in 1865 is : 25.05 – 8.29 = 16.67
- The difference between the Moving Average temperature trends of Riyadh and global in 1885 is : 25.10 – 8.05 = 17.05
- The difference between the Moving Average temperature trends of Riyadh and global in 1905 is : 24.82 – 8.24 = 16.58
0.00
5.00
10.00
15.00
20.00
25.00
30.00
TemperatureTemperatureTemperatureTemperatureTemperatureTemperatureTemperatureTemperature
YearsYearsYears Years
Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global Temperature in Riyadh vs global
local_avg_templocal_avg_templocal_avg_templocal_avg_temp local_avg_templocal_avg_temp local_avg_temp local_avg_temp
global_avg_tempglobal_avg_tempglobal_avg_tempglobal_avg_tempglobal_avg_temp global_avg_tempglobal_avg_temp global_avg_temp global_avg_temp
- The difference between the Moving Average temperature trends of Riyadh and global in 1925 is : 25.16 – 8.57 = 16.59
- The difference between the Moving Average temperature trends of Riyadh and global in 1950 is : 25.29 – 8.62 = 16.67
- The difference between the Moving Average temperature trends of Riyadh and global in 1975 is : 25.45 – 8.79 = 16.66
- The difference between the Moving Average temperature trends of Riyadh and global in 2000 is : 26.44 – 9.49 = 16.95
- The difference between the Moving Average temperature trends of Riyadh and global in 2013 is : 27.78 –9.61 = 18.17
We noted the temperature increasing between Riyadh and Global. The overall trends either global or Riyadh are increasing gradually day by day. World is getting hotter based on the trends above.
Correlation Coefficient:
It is used to measure how strong a relationship between two variables:
correlation coefficient between global and Riyadh temperature trends :
r = (171*(5659.97)-(4200.18*1459.79))/ sqrt(54763.64712*19033.3326)
r= 1.59
The correlation coefficient between global and Riyadh temperature trends is 1.59 which indicates strong positive relationship among them.
Conclusion:
In conclusion, we can depict that the temperature of globe has been rising exponentially and local area temperatures are also increasing at a rate similar to that of globe in the past century.
Resources files: Udacity
