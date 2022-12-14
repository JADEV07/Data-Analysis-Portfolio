# Google Data Analytics: Capstone Project
### Cyclistic Bike Share

## Project Overview
A fictional bike-sharing company, **Cyclistic**, has hypothesized that maximizing the number of annual members, versus casual riders, is the key to their future growth. In order to build a new marketing strategy aimed to convert casual riders into annual members, the marketing analyst tems wants to know:
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would causal riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

I will be answering the first question using the 6 steps of data analysis taught in the Google Data Analytics course; ask, prepare, process, analyze, share, and act.


## Ask
  
The Cyclistic executive team is concerned with maximizing their future growth as a company. Lily Moreno, the director of marketing, is concerned with ensuring this growth by creating a marketing strategy designed to convert casual riders of Cyclistic into annual members. The marketing analytics team, which I am a member of, are concered with using our data to answer the three above questions, and use the answers to guide the marketing program.  
  
The current task is to analyze the data and identify key behavioural differences between casual riders and annual members in order to present reccomended next steps to the company.  
  
## Prepare
  
The data used in the project comes is stored in AWS (Amazon Web services). I am using only the past 12 months of trip data, beginning in 2020-06 and ending in 2021-05.
The data is collected directly from Cyclistic and has been made available by Motivate Internation Inc. under [this license](https://www.divvybikes.com/data-license-agreement). The data has been anonymized and no personally identifiable information has been included in the data.  While this will prevent analysis which would examine specific personal traits of individual riders, such as individual history or areas of residence, there is still enough data to identify certain behaviours.  
  
## Process (Data Cleaning)
  
The primary tools for my analysis are Microsoft SQL Server, and Google Sheets.  
  
The extensive report for the cleaning process can be found [here](https://github.com/JADEV07/Data-Analysis-Portfolio/blob/main/EDA%20/R/Cyclistic-Analysis/Cleaning_Report.md)

In summary I made the following changes:  
  
* Removed duplicate rows
* Removed rows with null values concerning start and end stations
* Excluded rows reporting electric bike testing
* Excluded geographical coordinates
* Ensured consistency in datatypes across variables
* Altered variable names
  * bike used during ride = `bike_type`
  * user membership status = `user_type`
* Created a column to report duration of each ride
* Excluded trips lasting less than 1 minute, or over 24 hours
  
  
## Analyze
  
A full summary of my analysis process can be found [here](https://github.com/JADEV07/Data-Analysis-Portfolio/blob/main/EDA%20/R/Cyclistic-Analysis/Analysis%20Journal.md).  
  
I explored several variables for differences in behaviour between annual members and casual riders:
* use of bicyle types
* prefered month of ride
* prefered day of week
* usual length of ride
* most visited stations
  
I created several early draft visualizations. Below are some examples.  
  
![image](https://user-images.githubusercontent.com/87314229/126211131-7b051739-a4e0-467e-8bbf-2b534d3b0972.png)  
  
![image](https://user-images.githubusercontent.com/87314229/126211179-c4a33472-94f7-4c7d-867f-7624812e897b.png)  
  
![image](https://user-images.githubusercontent.com/87314229/126211208-d419afe5-0c8e-42d0-b700-09383505bd03.png)


## Share
![image](https://user-images.githubusercontent.com/87314229/126376705-d7dd7b8a-79ec-41b6-a2bd-2aa5d0933a9e.png)  
*(Cyclistic Dashboard, measuring behavioural differences between casual riders and annual members)*  
  
Key notable differences: 
* Casual riders tend to ride 10+ minutes longer than annual members  
* Casual riders favour the weekend days, Saturday and Sunday
* Casual riders ride the most in July and August and the least in January and Feburary  
  
  

## Act
My recommendations for the marketing strategy are as follows:
1. Offer discounted annual memberships in the months leading up to the summer months
2. Member exclusive deals on weekends, discounted ebikes, prebooking etc.
3. Aim advertising intiatives majorly in top 20 casual heavy stations
