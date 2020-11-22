--- 
title: "COVID-19 daily testes"
author: "Beatriz Farrugia"
date: "17/10/2020"
output: html_notebook
---
<p>#In this exercise, we are going to do 3 things:
<p> ##1- To sum how many people were tested since March
<p>##2 - To sum how many people tested positive since March
<p>##3- Check how many people tested positive in each day of the week.


#Firstly, we need to download the dataset (https://healthdata.gov/dataset/covid-19-daily-testing-person), from Health Data.gov website.

#Then, we use the function read.csv to import the dataset, adding "string as factor =false".

```{r}
read.csv("COVID-19_Daily_Testing_-_By_Person.csv",stringsAsFactors=FALSE)
```

#To grab the data, we create the variable "dailytests"

```{r}
dailytests<-read.csv("COVID-19_Daily_Testing_-_By_Person.csv")
```

#To discover the type of object, we use "typeof". In this case, the dataset is a list.

```{r}
typeof(dailytests)
```
#To discover details about the firsts rows and columns, we use "head":
```{r}
head(dailytests)
```
#Now, we are going to create a variable with a specific column:

```{r}
days<-dailytests$Day
```

#And another variable for the the column "People Tested Total"

```{r}
totaltests<-dailytests$People.Tested...Total
```

#The last one is for the column "People Positive Tested Total"
```{r}
positivetests<-dailytests$People.Positive...Total
```

#Now we are going to sum how many people were tested since March:
```{r}
sumtotalpeopletested<-sum(totaltests)
print(sumtotalpeopletested)
```
#And how many people tested positive since March:

```{r}
sumtotalpeoplepositive<-sum(positivetests)
print(sumtotalpeoplepositive)
```

##Creating a chart about the Positive tests since March

```{r}
barplot(height=positivetests)
```

#Then, we can go to our third task: check how many people tested positive in each day of the week since March. For this task, we need to use the function aggregate:

```{r}
final <- aggregate(dailytests$People.Positive...Total,
                 by = list(dailytests$Day),
                 FUN = sum)
```

#To print the result:
```{r}
print(final)
```
#And, finally, we can sort this result:

```{r}
sort(final$x, decreasing = TRUE)
```

