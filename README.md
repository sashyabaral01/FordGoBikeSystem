# Ford GoBike System Data
## by Sashya Baral


## Dataset
I used the Ford GoBike System Data dataset. The source of my data from the Udacity Project Information page. The data consisted of the following rows and columns:
0   duration_sec              
1   start_time                
2   end_time                  
3   start_station_id         
4   start_station_name        
5   start_station_latitude   
6   start_station_longitude  
7   end_station_id           
8   end_station_name        
9   end_station_latitude     
10  end_station_longitude    
11  bike_id                    
12  user_type                 
13  member_birth_year        
14  member_gender            
15  bike_share_for_all_trip  183412 non-null  object 
I performed several wrangling steps. I first removed the duplicate data entries (though there were none), then I dropped missing data. After that, I removed unecessary columns that were not needed for analysis. The rows I removed were the following
I kept the following rows:
duration_sec       
start_time          
end_time
user_type          
member_birth_year  
member_gender 
After removing several rows, I converted the duration_sec into duratin_min because it is easier to understand for me. Then I converted start_time to a DateTimeObject. After converting it to a DateTimeObject, I created new columns such as start_hour and start_day. I then created a new column called time of day start where I took the start_hour and classifed each entries as either Morning, Afternoon, Evening, Night. 
To get rid of outliers, I used a method I found on Stackoverflow. This method calculates the Z score to remove outliers from the data. I calculated the z for the bike duration time and the member birth year. 

## Summary of Findings
I made several discoveries with FordGoBike Data System. They include the following:
1. The most popular time of day to go biking: I found it to be the morning
2. The start hour distribution of people who go biking has the highest distribution at around 9 AM
3. The most popular day of the week to go bike riding is on Thursday
4. Among all the bike riders with the FordGoBike company, around 75% of users are males, 23.4% of users are females, and 2.1% is the other gender
5. 90% of bike users with the FordGoBike company are subscribers, and 10% of the users are customers
6. People born in the late 1980s and early 1990s had the highest count among all age distribution for the Bike Users
7. There was no evidence of a relationship between the age of a biker and the duration that they biked.
8. The average birth year of a customer and a subscriber was around 1985
9. The average male bike user was 1983, for females, the average birth year was 1986, and the average birth year for other is around 1984.
10. The most popular time for males to go biking is the in the morning. For females, the most popular time is the morning as well. The least popular time for males to go biking is at night, and it is the same for females as well. For other, the most popular time appears to be the evening, and the least popular is the night. The order in popularity for males to go biking from most popular to least popular is morning, evening, afternoon, then night. For females it is morning, evening, afternoon, then night. For other, the order from most popular to least popular is Evening, Afternoon, Morning, then Night.
11. The most popular day of the week for males to go biking is Thursday, and it is the same for females as well. For the other gender, Thursday is the most pouplar as well. The least popular days for males, other gender, and females is the weekend (Saturday and Sunday)
12. Other gender biker users had the highest average biking duration of around 11.89 minutes, females came in second with an average of around 11.5 minutes, and males came in last with an average of around 10.19 minutes

13. On all days of the week except for Monday, the average trip duration was the highest for the other gender, then the average duration was second highest for females, and men came in last. On Monday, females had the highest average duration time, then the other gender, and males were last in average duration time for biking. For all days of the week, the other gender had the highest standard deviations, then females had the second highest standard deviation, and men had the least standard deviation. 

14. Female customers had the highest average duration minute for bike riding, and male customers came in second, and in last other gender customers came in last. The average duration minutes for biking among subscribers was the highest in the other gender, then females subscribers were second in average duration minute in biking, and male subscribers came in last for the average duration bike riding. Female customers had the highest average biking duration, male customers had the second highest, other gender customers had the third highest, other gender subscribers came in fourth for average biking duration, female subscribers came in fifth for average biking duration, male subscribers came in last.

15. During night time, the other gender had the highest average biking duration of around 13 minutes. After other, females had the second highest biking duration of about 11 minutes, and men came in last with an average biking duration of about 9 minutes
In the evening, both female and other had about the same average biking duration. This is around 11 minutes. Men came in last with about 10 minutes. 
In the afternoon, the other gender had the highest average duration minute of around 13 minutes, and females had around 12.9 as their average biking duration minute, and in last, men had their average biking duration of about 10 minutes
In the morning, the other gender and females had the same average biking duration of about 11 minutes, and males came in last with an average biking duration of 9 minutes. 
    


## Key Insights for Presentation
For the Presentation analysis, I am looking into analyzing the bike users' genders in depth. I am looking at the relationship between the bike users' gender and other variables. Some of the insights I am investigating for the presentation include the gender proportion of all the bike users, the average biking duration for different genders, and the average biking duration for different genders from different days of the week