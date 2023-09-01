# -C-Users-kirub-Downloads-Final_Project_Final.twbx-

A.	Questions Addressed.

1.	Sheet 1. How much of an effect does Change Susceptibility have on BMI and Fitness? 
2.	Sheet 2. Was the sleep intervention more effective for quality of sleep, hours of sleep or neither? 
3.	Sheet 3. Can BMI and Sleep Quality be Used as a predictor for performance?
4.	Sheet 4. How engaged are remote workers?
5.	Sheet 5. Which demographics can provide insight into employees’ smoking levels? 
6.	Sheet 6. Which employees are more likely to stay with the company and is remote work a factor? 

B.	Calculated Fields.

1.	BMI Difference. In considering the impact of Change Susceptibility on BMI, this field considers the Pre-BMI and Post-BMI variables to determine the effect of the BSR health intervention on employee BMI (Sheet 1). BMI Difference is also considered in relation to employee performance (Sheet 3). We calculated this value by subtracting the Post-BMI from the Pre-BMI. 

Post-BMI – Pre-BMI

2.	Daily Exercise Difference. We subtracted the Pre-Daily Exercise (Min) from the Post-Daily Exercise to calculate the overall difference in exercise. This field provides a scale for us to determine the health intervention’s effects on employee fitness, which are ultimately assessed in relation to Change Susceptibility (Sheet 1). 

[Post: Daily exercise]-[Pre: Daily exercise (Min)]

3.	Total Change Commitment. To assess overall Change Susceptibility, we added the employee’s responses to each of the Change Commitment questions. These five responses to Likert-style questions provided a scale for us to evaluate openness to change in terms of BMI, sleep, and remote work (Sheet 1, Sheet 2, Sheet 4).

[Change commitment 1 (1-5)]+[Change commitment 2 (1-5)]+[Change commitment 3 (1-5)]+[Change commitment 4 (1-5)]+[Change commitment 5 (1-5)]

4.	Total Change Readiness. Similar to our calculation for Total Change Commitment, we took the sum of responses to Change Readiness questions to ultimately consider variables in relation to Change Susceptibility (Sheet 1, Sheet 2, Sheet 4).

[Change readiness 1 (1-5)]+[Change readiness 2 (1-5)]+[Change readiness 3 (1-5)]+[Change readiness 4 (1-5)]+[Change readiness 5 (1-5)]

5.	Change Susceptibility. Calculated by adding Total Change Commitment to Total Change Readiness, we used Change Susceptibility as a predictor for BMI and sleep improvement (Sheet 1, Sheet 2). Additionally, we used Change Susceptibility as a filter for considering its effect on employee engagement for in-person and remote workers (Sheet 4).

[Total Change Commitment]+[Total Change Readiness]
6.	Quality of Sleep Difference. To obtain a metric for examining openness to change in relation to sleep quality, we subtracted the Likert-scale response for pre-intervention quality of sleep from that for post-intervention quality of sleep (Sheet 2). We also considered this metric in relation to performance (Sheet 3).

[Post: Quality of sleep]-[Pre: Quality of sleep]

7.	Hours of Sleep Difference. Examined alongside Quality of Sleep Difference, this field demonstrates the heath intervention’s effects of sleep quantity. This metric helps us answer the question of which incentive was more effective in improving sleeping habits (Sheet 2). 

[Post: Hours of sleep]-[Pre: Hours of sleep]

8.	Change Susceptibility Label. We created this field to assign Likert-style values to our Change Susceptibility scale. Given that the summed responses range between 14-42, we used a range of six to divide the response categories along the scale. This field ultimately allows us to examine how openness to change impacts employee engagement (Sheet 4). 

IF [Change Susceptibility] <18 THEN "Firmly Against Change"
ELSEIF [Change Susceptibility] >=18 AND [Change Susceptibility] <24 THEN "Moderately Against Change" 
ELSEIF [Change Susceptibility] >=24 AND [Change Susceptibility] <30 THEN "Neutral"
ELSEIF [Change Susceptibility] >=30 AND [Change Susceptibility] <36 THEN "Moderately Open to Change"
ELSEIF [Change Susceptibility] >=36 THEN "Firmly Open to Change"
END

9.	Engagement Rating. In evaluating whether remote workers are less engaged than in-person workers, we summed Likert-style responses to questions of employee engagement (Sheet 4). This value includes the pre-intervention and post-intervention evaluations.  

([Post Engagement question 1]+ [Post Engagement question 2]+[Post Engagement question 3]-[Pre Engagement question 1]-[Pre Engagement question 2]-[Pre Engagement question 3])

10.	Difference in Smoking. We calculated the difference in cigarette consumption to examine the health intervention’s effects (Sheet 5). With this metric, we can see which demographic groups were the most affected by the intervention. 

[Pre: Smoking]-[Post: Smoking] 

11.	Satisfaction Questions. In taking the average of Likert-style responses to satisfaction-based questions, we were able to assess whether working remotely impacted an employee’s desire to stay with the company (Sheet 6).  

([Pre Satisfaction question 1]+[Pre Satisfaction question 2]+[Pre Satisfaction question 3]+[Post Satisfaction question 1]+[Post Satisfaction question 2]+[Post Satisfaction question 3])/6
