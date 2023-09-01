# -C-Users-kirub-Downloads-Final_Project_Final.twbx-
Through our research with BSR Insurance’s data, we examined how susceptibility to change affects well-being. We also investigated its impact on fitness interventions, BMI, and exercise levels, along with assessing how these interventions impact in-person and remote work dynamics regarding employee satisfaction and engagement. Using the employees’ Likert-based responses to questions of change readiness and commitment, we identified that Change Susceptibility is a key component in highlighting disparities in willingness, interventions, and overall performance.
Referring to the first and second sheets in Tableau, we examined Change Susceptibility in relation to health improvement, specifically in terms of fitness and sleep. The tree map demonstrates the relationship between an employee’s BMI variation and their receptivity to change, as well as daily exercise levels and receptivity to change. In comparing results before and after the intervention, the visualization reveals that employees more receptive to change tended to have a larger difference in BMI compared to those with higher BMIs who were moderately resistant to change. Meanwhile, individuals neutral to change showed minimal shifts in both factors. Under a similar scope, the second correlation shows that higher levels of Change Susceptibility resulted in greater sleep improvement. This correlation also indicates that perhaps the quality-based intervention was more effective than those focused on quantity of sleep. Ultimately, both visualizations demonstrate the significance of Change Susceptibility in monitoring improvement based on sleep and fitness-based interventions. 
The third visualization encompasses the intersection between BMI and sleep quality while observing the effects on performance. This addresses the question of whether BMI and sleep quality be used as a predictor for performance. Examining the bar chart, it becomes evident that employees with the least positive change in BMI and sleep quality exhibited the lowest performance levels. Conversely, those with the lowest BMI and highest sleep quality demonstrated the greatest increased performance. 
While previous visualizations show an improvement in health through Change Susceptibility, it is important to consider the effects of implementing the health pilot program to employees who work from home. We evaluated this by questioning the engagement levels of remote employees. In a histogram based on reported levels of engagement, we noticed that remote workers followed a more right-skewed distribution than that for in-person workers. This suggests that a greater number of remote workers tended to be less engaged compared to their in-person counterparts. Applying the lens of Change Susceptibility to this histogram, we see that employees who were firmly open to change were more likely to be engaged in work. As a result, we can infer that implementing the health intervention would be successful for remote workers, so long as BSR Insurance implements strategies of increasing Change Susceptibility. 
Based on the anticipated cost-savings and improved productivity, an organization-wide rollout of the health pilot program is recommended. However, to optimize its impact, it is essential to ensure holistic adoption of the process. This can be done by two primary influencing factors. Because middle management serves as the connective tissue between upper executives and the individual contributors of the workforce, their buy-in is pivotal. Furthermore, requesting a verbal commitment to the program from the participant in front of their coworkers will enhance the probability of buy-in as it involves an active, public, and freely chosen to partake. 
Appendix

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
