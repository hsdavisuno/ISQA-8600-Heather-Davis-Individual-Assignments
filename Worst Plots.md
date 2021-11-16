# Worst Plots

Author: Heather Davis

## Plot 1: HFS Facility, Age, and Gender Identity


```{r age, facility, gender_identity}
ggplot(data = HFS_Data) + geom_point(mapping = aes(x = age, y = facility, color = gender_identity))
```

![image of a scatterplot with facility as the y-axis, age as the x- axis, and a gender identity legend](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/ageFacilityGenderID.png)

Although I like how putting the facility labels on the left make them more readable, I think this plot needs the following to make it more understandable:


* The facilities need to be grouped to be able to spot patterns. It's difficult to see what is happening here with so many labels.

* The colored dots are too hard to read.The colors blend together. 

* The plot is trying to do too much simultaneously. Gender identity and age by facility. It should be broken up into two plots. 

## Plot 2: HFS event_name, total_duration)

```{r event_name, total_duration_num}
ggplot(data = HFS_Data) + geom_point(mapping = aes(x = event_name, y = total_duration_num))
```
![image of a scatterplot with total duration number as the y-axis and event name as the x- axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/eventNameTotalDurationNum.png)

I had several of my first plots turn out this way. I think this plot needs the following to make it more understandable:


* The events need to be grouped into types and the labels need to be angles. There are too many.
* The outliers at the top need to be removed because it is difficult to see what is happening with the data while it is scrunched down at the bottom of the plot. 

## Plot 3: Total Duration and Record ID


```{r }
ggplot(data = HFS_Data) + geom_point(mapping = aes(x = recordID, y = total_duration_num))
```
![image of a scatterplot with total duration number as the y-axis and recordID as the x- axis](https://github.com/hsdavisuno/ISQA-8600-Heather-Davis-Individual-Assignments/blob/main/recordIDTotalDuration.png)

This one is just silly. We need to just throw it away. It does nothing. It has no purpose. 

* The outliers at the top need to be removed because it is difficult to see what is happening with the data while it is scrunched down at the bottom of the plot.

* Having a scale for an identifier just doesn't make sense. 
