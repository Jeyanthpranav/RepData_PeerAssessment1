
Activity monitoring devices : Assignment 1 Reproducible Research

##Introduction

It is now possible to collect a large amount of data about personal movement using activity monitoring devices such as a Fitbit, Nike Fuelband, or Jawbone Up. These type of devices are part of the "quantified self" movement - a group of enthusiasts who take measurements about themselves regularly to improve their health, to find patterns in their behavior, or because they are tech geeks. But these data remain under-utilized both because the raw data are hard to obtain and there is a lack of statistical methods and software for processing and interpreting the data.

This assignment makes use of data from a personal activity monitoring device. This device collects data at 5 minute intervals through out the day. The data consists of two months of data from an anonymous individual collected during the months of October and November, 2012 and include the number of steps taken in 5 minute intervals each day.

##Data

The data for this assignment is downloaded from the course web site.

The variables included in this dataset are:

- steps: Number of steps taking in a 5-minute interval (missing values are coded as NA)
- date: The date on which the measurement was taken in YYYY-MM-DD format
- interval: Identifier for the 5-minute interval in which measurement was taken

There are a total of 17,568 observations in this dataset.

##Loading and preprocessing the data

##What is mean total number of steps taken per day?

Missing values in the dataset are ignored.

The total number of steps taken per day is calculated and histogram of the total number of steps taken each day is shown below,

The mean and median of the total number of steps taken per day is 


## What is the average daily activity pattern?

##Imputing missing values

Note that there are a number of days/intervals where there are missing values (coded as NA). The presence of missing days may introduce bias into some calculations or summaries of the data.

In order to visualize in which variable the NAs are

##Strategy for filling in all of the missing values in the dataset

The following strategy is chosen: for any NA is the step variable, the mean (of steps) of the corresponding interval is taken as the replacing value.

The 'mn_int' contains the mean for each single interval calculated over the 61 days. The right value coming from 'mn_int' is going to be used to replace the NA at the same interval.


Below is a histogram of the total number of steps taken each day. The mean and median total number of steps taken per day are reported.

In order to compare the new values with the “old” values:

It confirms there is no more NAs in the steps variable.

##Are there differences in activity patterns between weekdays and weekends?

A new column is added to the dataframe, this column will contain the factor “weekday days”“ or "weekend days”.


In order to visualize the difference bewteen weekends and days of the week, a new dataframe is created to be usable by the lattice package. First, the data are calculated:

Then the dataframe is prepared and the plot is plotted !

It can be observed that there is a small difference between the period.



