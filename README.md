# GENDER-CLASSIFICATION-REPORT-1

# CRASH_DATA REPORT PROJECT3

# PROBLEM STATEMENT

This Python Dashboard visualization helps to analyze the Crash/Accident details in some part of the United state of America(USA).This Data gives a thorough research about the crash calamities in the states resulting from different road users at different occassions and days using some parameters to calculate and visualize the charts,the chart talks about varis method in which accident occurs.


# TASK TO SORT 

- Total number of accident for each day  
- Average speed for each road user  
- Total number of accident for each road user
- Total number of accident for each gender  
- Average age for each road user 
- Total number of accident for each day of the week


![Screenshot (2)](https://github.com/user-attachments/assets/ea37d8a3-7453-4f02-b0ef-b66777a6e0b2)


# LIBRARY USED

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

1. TOTAL NUMBER OF ACCIDENT FOR EACH DAY: 

- Accident=crash_data.groupby("Dayweek")["Dayweek"].count()
- Accident
- name=Accident.index
- number=Accident.values

2. AVERAGE SPEED FOR EACH ROAD USER:
- crash_data["Speed Limit"]=crash_data["Speed Limit"].fillna(0)
- crash_data["Speed Limit"]=crash_data["Speed Limit"].replace({"Unspecified":0,"<40":40}).astype(int)
- name0=speed.index
- number0=speed.values

3. TOTAL NUMBER OF ACCIDENT FOR EACH ROAD USER:
- total_Accident_user=crash_data.groupby("Road User")["Road User"] - count()
- total_Accident_user
- name1=total_Accident_user
- number1=total_Accident_user

4. TOTAL NUMBER OF ACCIDENT FOR EACH GENDER:  
- total_accident_gender=crash_data.groupby("Gender")["Gender"].count()
- total_accident_gender
- name2=total_accident_gender.index
- number2=total_accident_gender.values

5. AVERAGE AGE FOR EACH ROAD USER:
- total_Accident_user=crash_data.groupby("Road User")["Road User"]. count()
- total_Accident_user
- name2=total_Accident_user
- number2=total_Accident_user

6. TOTAL NUMBER OF ACCIDENT FOR EACH DAY OF THE WEEK:
- accident_days_week=crash_data.groupby("Day of week")["Day of  week"].count()
- accident_days_week
- name4=accident_days_week.index
- number4=accident_days_week.values  

# SCREENSHOT OF THE SUBPLOT
- fig,crash_data=plt.subplots(nrows=2,ncols=3,figsize=(14,8))
- fig.suptitle("Crash_Data",fontsize=20,fontstyle="italic",fontweight="bold",c="r")
- crash_data[0,0].barh(name,number)
- crash_data[0,1].bar(name0,number0)
- crash_data[0,2].plot(name1,number1)
- crash_data[1,0].pie(number2,labels=name2,autopct="%1.0f%%",shadow=True,explode=[0,0.1,0])
- crash_data[1,1].scatter(name3,number3)
- crash_data[1,2].bar(name4,number4)
- crash_data[0,0].set(title="Accident for each the day")
- crash_data[0,1].set(title="Average speed")
- crash_data[0,2].set(title="Accident for each road user")
- crash_data[1,0].set(title="Accident for gender")
- crash_data[1,1].set(title="Average age for each raod user")
- crash_data[1,2].set(title="Accident for each day of the week")
- plt.tight_layout()
- plt.savefig("Crash_Data.png")
- plt.show()

![Crash_Data](https://github.com/user-attachments/assets/584ef051-c23c-4bdf-bd9c-7e006fb23fb7)




























