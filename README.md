
Statistical Analysis of Crime Data and Socio-Economic Factors in the City of Chicago

# Abstract:
This research paper aims to provide a comprehensive statistical analysis of the relationship between crime rates and socio-economic factors in the City of Chicago. Utilizing a crime dataset spanning 2001 to 2023 (focusing particularly on 2018 - 2023), various statistical methods, including data visualizations, regression analysis, and more, were employed to uncover insights into the intricate dynamics between crime and socio-economic indicators. 

# 1. Introduction:
The City of Chicago stands as an urban landscape marked by its diversity, vibrant culture, and distinctive neighborhoods. Amidst its dynamic tapestry, understanding the underlying factors influencing crime rates remains a pivotal concern for policymakers, law enforcement agencies, and urban planners. This statistical analysis aims to delve into the relationship between crime rates and various socio-economic determinants within Chicago’s neighborhoods.
Context and Significance
Chicago, as one of the largest metropolitan areas in the United States, has grappled with challenges related to crime and community well-being. While crime rates fluctuate across different states, understanding the socio-economic underpinnings driving these variations is imperative. Exploring how factors such as educational attainment, employment status, income levels, and other socio-economic metrics correlate with crime rates can provide critical insights.
Objectives of the Analysis
This study endeavors to:
•	Assess the relationship between the crime rates and socio-economic variables across different areas within Chicago.
•	Investigate whether socio-economic factors, such as unemployment rates, educational attainment, or income disparities, exhibit associations with crime rates.
•	Identify potential patterns or correlations that could aid in formulating targeted interventions or policies aimed at crime reduction and community development.
Methodology Overview
The analysis employs statistical tools, particularly regression analysis, to scrutinize the relationship between crime rates and socio-economic factors. Utilizing datasets encompassing crime statistics and socio-economic metrics across various communities within Chicago, the study seeks to ascertain the impact of these variables on crime rates.
Contribution and Implications
By unraveling the complex interplay between socio-economic conditions and crime rates, this analysis aspires to contribute valuable insights that could inform evidence-based policymaking and community initiatives. Understanding the factors influencing crime rates can guide targeted interventions aimed at fostering safer, more equitable neighborhoods throughout Chicago.

# 2. Literature Review:
This section reviews prior and existing studies on the topic that have explored the intricate relationship between crime rates and socio-economic factors within urban settings, specifically focusing on research related to the City of Chicago. By examining the methodologies, findings, and limitations of these studies, this review aims to contextualize the current research and pinpoint gaps that necessitate further investigation.
Socio-Economic Determinants of Crime Rates and Gaps in the Existing Literature
Despite the breadth of existing research, certain gaps and limitations persist. Many studies tend to focus on crime rates, overlooking the impact of socio-economic conditions on crime rates in urban areas. Furthermore, there remains a dearth of comprehensive studies that account for temporal variations and changing socio-economic dynamics in Chicago’s neighborhoods over time. In this work, I hope to identify a strong association between low educational attainment levels and increased criminal activities. 
Methodologies Employed in Prior Studies
Previous research on crime rates often employed diverse methodologies, ranging from regression analysis to spatial mapping techniques. Studies such as Alqahtani, A. et al. (2019) utilized SAT SCAN to find the hot spots and do the clustering for the spatial data, while others like Monish, N. (2019) discussed how other authors like Chang, P. et al, leveraged AutoRegressive Integrated Moving Average (ARIMA) model to get short term forecasting of property crime in China.

# 3. Data Collection:
Data Source: This dataset is downloaded from Crimes - 2001 to Present | City of Chicago | Data Portal
Sample Space and Events:
a)	Sample Space: The dataset contains crime events in the city of Chicago from 2001 to Present.
b)	Events: The events related to the different crime types and socio-economic factors include:
1)	Crime Types: 
2)	Socio-economic Factors: These include variables in the dataset, such as ‘High……….., etc.
Data Cleaning / Preprocessing:
Data cleaning has been done to make analysis easier.
•	The dataset contains crime events in the city of Chicago from 2001 to Present.
•	Missing values were removed and filled accordingly. 
•	Variables have been converted to categorical variables.

# 4. Exploratory Data Analysis (EDA):
Here, I tried to make sense of the data by exploring the distribution of crime types, temporal trends in crimes, and correlation of crime rates with demographic factors like poverty, education, and unemployment.
A summary of the statistics with several visualizations is shown below.
Several key insights were derived from the exploratory data analysis utilizing data visualization charts such as scatter plots, histogram, line plots and box plots. 
•	The scatter plot helped show the crime distribution across the city. It was also used to visualize the relationship between unemployment and the number of crimes within the city.
•	Histogram was employed to show the distribution of crimes per community area.
•	Box plot was also utilized to visualize the distribution of crimes across community areas.
The scipy.stats.pearsonr() function in Python’s SciPy library allowed me to calculate the Pearson correlation coefficient between the two variables and obtain the associated p-value for testing the significance of the correlation.


           
 	Fig. 1. Crime distribution (2018 to 2023) 	Fig. 2. # of crimes by day of week

      
Fig. 3. # of crimes per month (’01 to ’18)		Fig. 4. # of crimes per month (2018 to 2023)


         
	Fig. 5 # of crimes by type				Fig. 6 # of crimes by location

    
Fig. 7. Crime distribution per community area	        	Fig. 8. Crime distribution across areas 
          
	Fig. 9. Unemployment vs # of crimes		Fig. 10. No diploma vs # of crimes

# 5. Descriptive Statistics:
Central Tendency Measures
•	Mean values:
	Number of Crimes          1058.083747
	Below Poverty Level         24.986940
	Unemployment                15.296366
	No High School Diploma      22.682410
	
•	Median values:
	Number of Crimes          519.0
	Below Poverty Level        25.3
	Unemployment               16.7
	No High School Diploma     22.0
	
•	Mode values:
	Number of Crimes          5910.0
	Below Poverty Level         27.0
	Unemployment                21.0
	No High School Diploma       3.4
	
Variability Measures
•	Variance values:
	Number of Crimes          1.952272e+06
	Below Poverty Level       1.001609e+02
	Unemployment              5.121867e+01
	No High School Diploma    1.437291e+02
	
•	Standard Deviation values:
	Number of Crimes          1397.237201
	Below Poverty Level         10.008040
	Unemployment                 7.156722
	No High School Diploma      11.988708
	
•	Range values:
	Number of Crimes          5909.0
	Below Poverty Level         58.3
	Unemployment                35.8
	No High School Diploma      55.8
	
Frequency Distribution
•	Frequency distribution of crimes by time-period:
	Day parts
	night        2618
	morning      2618
	afternoon    2618
	evening      2618
	Name: count, dtype: int64


# 6. Hypothesis Testing:
To perform my hypothesis test, I formulated the following.
Null Hypothesis (H0): There is no significant correlation between the average crime rates and unemployment in Chicago.
Alternative Hypothesis (H1): There is a significant correlation between the average crime rates and unemployment in Chicago.
Significance Level: A significance level of 0.05 is chosen to determine the threshold statistical significance.
Statistical Test: I chose to use the T-test to compare crime rates between unemployment and number of crimes and the result is shown below.
•	Pearson correlation coefficient: 0.16596566090484713
•	P-value: 0.0
•	The correlation is statistically significant.

# 7. Regression Analysis:
Ordinary Least Squares was employed for my regression analysis and the results are shown below. The R-squared and Adjusted R-squared values (-123.869 and – 123.870 respectively) are negative indicating    computational or numerical issues in the model. 

OLS Regression Results                             
=================================================================================
Dep. Variable:     crime_rate_per_capita   R-squared:                    -123.869
Model:                               OLS   Adj. R-squared:               -123.870
Method:                    Least Squares   F-statistic:                -1.004e+05
Date:                   Sun, 10 Dec 2023   Prob (F-statistic):               1.00
Time:                           19:32:36   Log-Likelihood:             5.4553e+06
No. Observations:                 202396   AIC:                        -1.091e+07
Df Residuals:                     202393   BIC:                        -1.091e+07
Df Model:                              2                                         
Covariance Type:               nonrobust                                         
==========================================================================================
                             coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------------------
const                     75.9250   2.82e-15   2.69e+16      0.000      75.925      75.925
Unemployment           -4.979e-14   1.57e-16   -316.286      0.000   -5.01e-14   -4.95e-14
No High School Diploma -7.708e-16    9.4e-17     -8.202      0.000   -9.55e-16   -5.87e-16
==============================================================================
Omnibus:                     7112.766   Durbin-Watson:                   0.000
Prob(Omnibus):                  0.000   Jarque-Bera (JB):             7963.090
Skew:                           0.460   Prob(JB):                         0.00
Kurtosis:                       3.311   Cond. No.                         79.6
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.

The Unemployment coefficient of -4.979e-14 suggests the expected change in the crime rate per capita for a one-unit increase in unemployment.
The coefficient for ‘No High School Diploma’ is approximately -7.708e-16, also indicating the expected change in the crime rate per capita for a one-unit increase in the number of individuals without a high school diploma.
Statistical Significance:
The p-values for both coefficients are shown as 0.000 (or very close to zero), indicating that they are statistically significant. However, the extremely small coefficient values might suggest numerical precision issues or possible collinearity problems between the independent variables.

# 8. Time-Series Analysis:
The study engaged in time series analysis utilizing a sequence of collected data points obtained at regular intervals over a specific timeframe The dataset integrated crime-related information with arrests data to explore potential disparities between reported crimes and corresponding arrests. Additionally, the investigation delved into the temporal spread or frequency of criminal activities, aiming to discern patterns in the occurrence of specific crimes.
This analytic endeavor held significance as it sought to delineate trends in the commission of crimes. The findings aimed to offer valuable insights, potentially aiding law enforcement agencies in devising strategic approaches to address and mitigate criminal activities. By identifying patterns and trends in the timing and prevalence of specific offences, this analysis aimed to provide a foundation for more effective prevention strategies and law enforcement interventions.
 the spread (or occurrence) of crime with regards to when certain crimes occurred the most. This was significant in that it would help to show a trend in how these crimes were committed and hopefully help provide a …for law enforcement to address and arrest the 

# 9. Findings and Discussion:
The analysis conducted revealed several key findings regarding the relationship between crime and socio-economic factors in the studies context. Notably, the analysis indicated a moderate correlation between the variable ‘Below Poverty Level’ and the ‘Number of Crimes’, suggesting a discernible association between areas characterized by higher poverty rates and increased crime incidences. This finding underscores the potential influence of economic deprivation on crime rates within the studied region.
In contrast, the correlations between ‘unemployment’, ‘No High School Diploma’ and ‘Number of Crimes’ exhibited a weaker but also positive association. Although these factors displayed some degree of correlation with crime rates, their impact might be less pronounced compared to the influence of poverty levels. The weaker correlations imply that while unemployment and educational attainment might have some influence on crime, other socio-economic or environmental factors could contribute more significantly to variations in crime rates.
These findings hold crucial implications for understanding the intricate interplay between socio-economic conditions and crime. They suggest that addressing poverty levels within communities could potentially serve to mitigate crime rates. Policymakers and law enforcement agencies might benefit from targeted interventions aimed at alleviating economic disparities, as this could contribute to reducing crime incidences.
However, it is important to note that while socio-economic factors play a role, crime is a complex issue influenced by various multifaceted determinants beyond these correlations. Therefore, a holistic approach considering additional contextual factors, community engagement, and tailored interventions remains essential in developing effective strategies to address crime.

# 10. Limitations:
Despite the insights gained from this analysis, several limitations merit consideration. Firstly, the analysis heavily relies on available dataset, which might exhibit limitations in terms of completeness, accuracy, or coverage. The dataset might lack certain crucial variables or contain missing values, potentially constraining the depth of the analysis and its overall reliability.
Secondly, inherent assumptions were made during the analytical process, particularly concerning relationships between variables or the absence of certain confounding factors. These assumptions, while necessary for the analysis, might introduce a level of uncertainty or oversimplification into the findings.
Moreover, potential biases could influence the results. For instance, the dataset might reflect biases due to underreporting or overrepresentation of specific types of crimes or demographics. Additionally, the analysis assumes stationarity or linear relationships between variables, which might not hold true in a dynamic and complex environment like crime patterns.
Furthermore, the scope of the analysis might not encompass all relevant socio-economic factors or external variables that could influence crime rates, leading to an incomplete understanding of the phenomenon.

# 11. Conclusion:
This project mainly focuses on statistical analysis of crime data and socio-economic factors. While the analysis offers valuable insights, these limitations underscore the need for caution when interpreting the results and highlight avenues for future research to address these constraints and enhance the robustness of analysis in similar contexts.
As already mentioned, key insights from this study identified moderate correlation between some independent and dependent variables and a higher correlation between low income and the number of crimes. By uncovering these associations, the study provides a foundation for targeted interventions and policy formulations aimed at addressing economic disparities to potentially curb crime rates. Future research efforts should focus on exploring causal mechanisms, considering additional variables, and employing robust methodologies to further advance this field of study. 

# 12. References:
[1]	Monish N, "Chicago Crime Analysis using R Programming ", International Journal of Scientific Research in Computer Science, Engineering and Information Technology (IJSRCSEIT), ISSN : 24563307, Volume 5 Issue 2, pp. 937-944, March-April 2019. Available at doi :  https://doi.org/10.32628/CSEIT1952173 Journal URL : http://ijsrcseit.com/CSEIT1952173
[2]	Alqahtani, Ayidh; Garima, Ajwani; Alaaid, Ahmad. (2019). “Crime Analysis in Chicago City.” Information Systems Department, University of Maryland Baltimore County, Baltimore, United States & CIS Department; Jordan University of Science and Technology, Irbed, Jordan.
13. Appendices:
Include any supplementary materials, additional analyses, or detailed information that enhances the understanding of the research.
