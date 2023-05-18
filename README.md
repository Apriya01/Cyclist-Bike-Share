# Cyclist-Bike-Share

# **Introduction**
      This case study is the ***[Capstone Project](https://www.coursera.org/learn/google-data-analytics-capstone)*** of ***[Google Data Analytics Professional Certificate](https://www.coursera.org/professional-certificates/google-data-analytics)***. This analysis is based on a fictional company called Cyclistic. it contains a Sophisticated, Clear, and Polished Cyclistic data and Data Visualization. The purpose of this script is to consolidate downloaded Cyclistic bikeshare data into a single dataframe and conduct simple analysis to help answer the key question: “In what ways do members and casual riders use Cyclistic bikes differently?”.In this case study I am working as a junior data analyst in the marketing analyst team at Cyclistic, a fictional bike-share company in Chicago.
      In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day.
      The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, my team wants to understand **how casual riders and annual members use Cyclistic bikes differently**. From the insights, our team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve our recommendations, so they must be backed up with **compelling data insights and professional data visualizations**.
       There are 3 pricing plans: single-ride passes, full-day passes, and annual memberships. **Customers who purchase single-ride or full-day passes are referred to as Casual riders. Customers who purchase annual memberships are Cyclistic members**.
        In order to answer the key business questions, I followed the steps of the data analysis process: **ask**, **prepare**, **process**, **analyze**, **share**, and **act**.


# **Ask**
>* **How do Annual members and Casual riders use Cyclistic bikes differently?**
>* The key stakeholders are:
     >  1. **Lily Moreno**, the director of marketing and my manager.
     >  2. **Cyclistic executive team**.  
* **First the Cyclistic executive team must approve our recommendations, so they must be backed up with data insights and data visualizations.**
* **Then from the insights of my analysis, my team will design a new marketing strategy to convert casual riders into annual members.**


# **Prepare**
* The **data** I used is ***[Cyclistic’s Historical Trip Data](https://divvy-tripdata.s3.amazonaws.com/index.html)*** to analyze and identify trends. 
* In this Dataset considered 3 years as 2020 (Apr-Dec), 2021(Jan-Dec) and 2022(Jan-Nov). So here, The **previous 12 months** data from **2021 January 1 to 2021 December** is used for analysis.
* The data is stored in **CSV** files. Each file contains **one month data**. Thus a total of **12** .csv files.
* The data is **structured data** ie., Organised data.
* The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are **appropriate**. 
* The data has been made available by **Motivate International Inc.** under this ***[license](https://www.divvybikes.com/data-license-agreement)***. 
* As this data is collected by a real bike sharing company in Chicago, there are no issues with **bias** or **credibility**. So its **Reliable**, **Original**, **Current** and **Cited** (as in ROCCC). I do not think its **Comprehensive** because this data lacks some information.
* As of data Integrity, its **Accurate**, **Consistent** and **Trustworthy**.

    > **Limitations**
    * The **data-privacy issues prohibit me from using riders’ personally identifiable information**. This means that I won’t be able to connect pass purchases to       credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.
    * The **financial information** such as each Ride Id ticket fare is not available.
    * If the personally identifiable information and financial information were available, I could have calculated whether the casual riders had spent more money 
      than if they opt for taking annual memberships.
    * This data does not contain data about the use of reclining bikes, hand tricycles and cargo bikes. It is said that about 8% of total riders use assistive 
      options. 
    * In this case specially three types of bikes are used i.e, Classic bike, Electric bike and Docked bike.


# **Process**
* For this data analysis, I used **EXCEL** and **TABLEAU**.
> EXCEL is used for Data Cleaning.
> Excel, Power query and Tableau are used for Data Analysis and Power point is used for Visualization.

    > **Cleaning Process**
    1. **Deleted** the below columns as they are irrelevant for my analysis.
      > Start Station Name
      > Start Station ID
      > End Station Name
      > End Station ID
      > Start Lat
      > Start Lng
      > End Lat
      > End Lng
    2. **Created** new column "**ride_length**". In that column, each row contains the difference between "starting time" and "ending time" columns in minutes.
    3. In the "ride_length" column created, many rows in some months contained **negative values**. Such errors happened because the "ending time" was earlier 
       than the "starting time" in their respective rows.
    4. All those rows containing negative "ride_length" are **deleted**. Those rows were **showing duplicate entries** in "ride_id" column.
    5. After deleting the irrelevant columns, **no blank cells** were found in the data.
    6. "ride_id" column is trimmed using "TRIM" function in excel to **remove unnecessary spaces** in cells.
   
   ![No Duplicate Rows](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/63df50c4-3451-44db-8dfc-690b501daf09)

     In Tableau, I checked the **Total Count of Ride Id** and **Distinct Count of Ride Id**. As both were **same**, means there are **no duplicate rows**.


# **Analyze**
* After cleaning process in EXCEL,the 12 CSV files were opened in **TABLEAU** and merged together using **UNION**, then analyzed and performed calculations.
    # **Analyzation of Data**
    
    ![Total Rider](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/6206ff21-1e09-48a3-adc7-cdfbd3fe9054)

    ![Total Rides](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/f68102e5-057e-44e1-9646-207590d577ea)
    
    ![Avg  Ride length_Monthly](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/ca23c2e6-a2c8-4a5d-a996-f160ee34c6ca)

    ![Avg  Ride length_Weekly](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/9ebb6228-b810-4d28-ac97-0d5f2566ce32)

    
  > # **Analyzing Rideable Type Usage**
    
    ![Rideable Type Usage](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/5eb490a4-3571-4450-93a0-09a3611bd567)

# **Share**

![Total Rides](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/2ba44fea-d336-486a-b048-41c02ff30d9c)

![Total Rides.png](attachment:08974cbb-3fd6-4f2f-9a1e-efd9a9f45435.png)
* We can see the total number of casual riders in a year are **slightly lesser** than annual members.

![No. of Rides (Monthly)](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/d3acffc1-4d30-4a7f-a427-54c91942c2f2)

![No. of Rides (Monthly).png](attachment:51041878-1579-46c7-ba1b-144d7b3d0240.png)
* It shows that the total number of riders **fall during winter season** and **rise during summer season**. The behaviour of casual riders and members **tend to 
  be the same** as the season changes.

![No. of Rides (Weekly)](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/17db2ce7-229b-4a2f-802b-8e17edf57acf)

![No. of Rides (Weekly).png](attachment:a7e298da-69ac-43d8-9246-f6860ac91c26.png)
* Here it shows **more casual riders** are using bike share on **Weekends** (ie., Saturdays and Sundays). But there are a fixed number of casual riders **using on 
  Weekdays**, may be commuting. While the number of members riding **tend to be same almost daily**.

![No. of Rides (Hours)](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/a4a9e424-da9c-4345-b7ba-7d1621235e33)

![No. of Rides (Hours).png](attachment:d7047b51-f3e7-46cb-8cdd-7d87ecb9a392.png)
* In a day, casual riders and members use bike share **more during afternoon**, **peak use during evening**. While in the **morning** time, the number of **casual   riders are way less than the members**.

  > # **Visualization of Average Ride Length**
  > ![Average Ride Length](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/c19f6232-6d54-404f-82ba-fe9dd1b52bf9)

    ![Average Ride Length.png](attachment:dab4f5a7-e8e3-4c87-a8f9-2485b8c5891d.png)
    * The average ride length of casual riders are **more than twice** of members. 

![Monthly Average Ride Length](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/3f8b0235-91a1-4230-b8cd-97569adffb42)

    ![Monthly Average Ride Length.png](attachment:82da72be-6fea-43f7-89ba-80ab6ed07aa8.png)
    * During the year, average ride length of casual riders are **more than twice** than members in all seasons.

![Weekly Average Ride Length](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/b63b1ede-26a9-4c22-a7a4-ee665110b5a5)

    ![Weekly Average Ride Length.png](attachment:072fe0ca-1b8c-4f10-9963-0b1d8fc7bd17.png)
    * In **Weekends** casual riders' ride length is **maximum** when compared to Weekdays. Members' ride length tend to be almost same in all Weekdays and      
      marginally higher in Weekends. 
      
   > # **Visualization of Rideable Type Usage**

  ![Rideable Type Usage](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/dd16fd6f-ed1b-46e9-83e0-5267581f1669)

    ![Rideable Type Usage.png](attachment:1eafd702-f155-4f3b-8f88-7979cfbcd1d2.png)
  
  
  ![users preference](https://github.com/Apriya01/Cyclist-Bike-Share/assets/126944168/5f64d6fd-846a-4402-a3d7-2117378ea28f)

  ![users preference.png](attachment:29f4f069-d005-49aa-9045-275f4451a11c.png)
    * **Most User's** are Prefered the **Classic bike** as in no. of **3.25mn users** other than two models of bike in both **Casual** and **Member** riders' 
        section.


# **Act**
**Conclusion**
> * Annual members and Casual riders use Cyclistic bike share **differently**.
> * The **average ride length** of causual riders are **more than twice** as of members.
> * From the **average ride length difference**, we can conclude that Annual members usually use bike share for **daily commuting**, while casual riders mostly 
    use bike share for **leisure rides** mostly **Weekends**.
> * But there are a **fixed number of casual riders** who use bike share for **commuting**.

**Additional Data to expand the findings**
* If the personally identifiable information and financial information were available, I could have calculated whether the casual riders had spent more money than 
  if they opt for taking annual memberships.
  
**Recommendations**
> * A **new Annual Membership package for Weekend usage only** will attract current Weekend casual riders.
> * **Promotions** aiming at **current Weekday casual riders** must be implemented as soon as possible. Those promtions must include the financial savings of 
    taking membership when compared to single passes and full day passes for a year long period.
> * A **Loyalty Program** for casual riders can be implemented, where **occasional membership fees discounts** must be given to casual riders with **high loyalty 
    points**.
