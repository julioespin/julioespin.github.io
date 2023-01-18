# NBA Analysis

<img src="images/HealthCare_Analysis_Cover.png"/>

## Let's Get Started!

As someone who has experience in the healthcare field, I thought that it would be interesting to analyze some healthcare data. In this project, I used SQL to analyze healthcare data and focused on getting insights into the following questions:

  - Do the majority of patients stay in the hospital for less than 7 days?


---

## The Data
I used [Tableau](https://public.tableau.com/app/profile/julio.espinoza/viz/21-22NBAAnalysis/21-22NBAAnalysis) to analyze 21-22 NBA data and the dateset can be found [here](https://www.basketball-reference.com/leagues/NBA_2022_totals.html).


---

## The Analysis
 
### NBA players performance on total points, total assists, & total rebounds. 

The first item I analyzed was the NBA players total points, assists and rebounds. I created a bubble plot that measures all three points of interest with assists and points being measured in the graph, rebounds measured by the size of the data point, and each color representing different player positions. 


<img src="images/NBA_Analysis_bubble.png"/>


We notice that point guards have the highest points and assists while centers have the lowest. We also notice a Nikola Jokic is an outlier having greater than usual rebounds, assists, and points compared to other players in his position as a center. 


### What medical specialties are doing the most number of average procedures?

The next item that I looked at was determining which medical specialties have the highest average number of procedures. Using the SQL statement below, I was able to find that information.

<img src="images/Healthcare_Analysis_medical_specialties.png"/>
------image of heatmap

The results provide a short list of 5 medical specialties that are most commonly used and have an average number of procedures greater than 2.5.


### Is the hospital treating patients of different races differently? Specifically with the number of lab procedures done?

To answer this question, I used a *JOIN* to combine two tables that share a common column and contain the information that I am looking for. One of the tables contains patient health and treatment information, while the other table contains demographic data. These two tables are related via patient_nbr column that is a unique patient ID number given to every patient.

<img src="images/Healthcare_Analysis_demographics.png"/>
------image of stacked bar chart

The results show that the average number of procedures range from 41.82 - 44.46, there is an unknown race (most likely not documented/recorded), and there does not appear to be a gap between the number of procedures between each race as the average number of procedures are similar. 


### Is there any correlation between the number of days stayed in the hospital to the number of lab procedures ordered? 

To answer the next question, I first assgined a category patients based on the number of procedures that they had. Lab procedures ranged from:

 - 0-24 as Few
 - 25-54 as Average
 - 55+ as Many
 
I used the SQL statement below to provide the results.

<img src="images/Healthcare_Analysis_procedures.png"/>
-----image of treemap

We notice that each patient is assigned as having few, average, or many procedures.



---

## Results and Recommendation

Using SQL, I was able to find interesting insights to the healthcare data. I found that the average patient stay is less than 7 days with most patients staying an average of 3 days; there are 5 medical specialties that are doing most number of the procedures on average; there does not appear to be a difference in the way that different races are treated; and there appears to be a relationship between the average length of a patient's stay and the number of procedures that they receive. 

In addition, I was able to create a list of patients who are African-American or have an "Up" to metformin; a list of patients who had an emergency but stayed less than the average time in the hospital; and a summary of the top 50 medication patients.

---

***I appreciate you making it to the end of the article. Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/jbespinoza/).***
