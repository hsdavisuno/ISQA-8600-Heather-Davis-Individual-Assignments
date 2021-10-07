# Data Exploration

# Variable Scatterplots
**General Location and Age**

![image of a scatterplot with general_location as the y-axis and age as the x-axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/1AgeandGeneralLocationScatterplot.png "Scatterplot 1")

    Code: ggplot(data = HFS.Service.Data) + geom_point(mapping = aes(x = age, y = general_location))
    
**Observations:** 


Temporary Lodging, Sanctuary Shelter, and Emergency Room - Hospital have very few points. Maybe they aren't tracking age or maybe they have very few clients. Residential Substance Use Treatment Facility, Place of Employment/Worksite, Inpatient Hospital, Homeless Shelter have a few clients. Most of the clients are in the following categories: Use When No Other Code Fits - Other, Telehealth - Video, Telehealth - Phone, Home, HFS Office and - are the categories have the most people. School skews to the lower end of the age categories, as one might expect. From a data-cleaning perspective, I would need to look into the field with no value at the bottom of the y-axis. 


**Age and Gender Identity**

![image of a scatterplot with age as the y-axis and gender_identity as the x- axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/2AgeandGenderIDScatterPlot.png "Scatterplot 2")

    Code: ggplot(data = HFS.Service.Data) + geom_point(mapping = aes(x = age, y = gender_identity))
    
**Observations:** 

As one might expect, the Man and Woman categories have a large amount of clients. The NA, and Not Obtained categories have a surprisingly large amount. Just a few in Other, Non-Binary, and Client Declined to Give and one in Two-Spirit, Other, and Female. For data cleaning, we would probably think about combining Female and Woman. 

# Scatterplot with Three Variables

![image of a scatterplot with general_location as the y-axis and age as the x-axis and a legend with general location](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/3AgeGenderandGeneralLocationScatterPlot.png "Scatterplot 3")

    Code: ggplot(data = HFS.Service.Data) + geom_point(mapping = aes(x = age, y = gender, color = general_location))
    
**Observations:** 

For this plot, I bullt on the age and gender plot by adding general_location. The data dictionary defines this field as "Classification of client's location at time of service". The color really helps pick out that "Telehealth - Video" is a popular location across age groups. Comparing 
Women and Men over 55, women appear to be higher users of this method than men. 


# Scatterplot with Two Variables and Trendline

![image of a scatterplot with total duration_num as the y-axis and age as the x-axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/4TwoVariableswithLine.png "Scatterplot 4")

    Code: ggplot(data = HFS.Service.Data) + geom_smooth(mapping = aes(x = age, y = total_duration_num))

**Observations:** 

For this plot, I needed two continuous variables to make it work without errors. I had trouble getting this to do both a scatterplot and smooth so I went with just smooth. I chose total_duration_num and age. The data dictionary description for the total_daration_num field isn't very descriptive but I think it is the duration of the service appointment. I thought it was interesting that the duration of the visit appears to peak with clients who are around age 40. If we looked into this further, we'd want to ask exactly what the total_druation_num field is.

# Faceted Plot with Two Variables

![image of a scatterplot with gender_identity as the y-axis and age as the x-axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/5TwoVariableFacetGrid.png "Scatterplot 5")

    Code: ggplot(data = HFS.Service.Data) + geom_point(mapping = aes(x = age, y = gender_identity)) + facet_grid(. ~ gender_identity)
    
**Observations:** 

I'm not sure this visualization provides me anything more than the gender_identity and age scatterplot. I didnt' see anything else to take away form this one. 

# Bar Chart

![image of a scatterplot with count as the y-axis and age as the x-axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/6CountofAgeBarChart.png "Scatterplot 6")

    Code: ggplot(data = HFS.Service.Data) + geom_bar(mapping = aes(x = age))
    
**Observations:** 

This chart is simple but very interesting - counting clients' ages. You can see the clients skew younger - and peak around 13 years old. There's another spike at 26 and 30. It would be interesting to see what services they were using at different ages. For data cleaning, we'd pprobably want to make sure we were counting each unique client and not counting an instance for every time the same client visited. 
