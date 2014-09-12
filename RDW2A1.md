---
title: "Reproducible Research: Peer Assessment 1"
output:
html_document:
keep_md: true
---

### Loading and preprocessing the data

```r
library(chron)
library(lattice)
setwd("C:/Users/Farhad/Documents/University/Coursera/Data Science  John Hopkins/4 - Reproducible Research/Homeworks")

Sys.time()
fURL="http://d396qusza40orc.cloudfront.net/repdata/data/activity.zip"
f<-read.csv(fURL,header=FALSE)
temp<-tempfile()
download.file(fURL,temp)
theData<-read.csv(unz(temp,"activity.csv"))
unlink(temp)
```




![plot of chunk clean data](figure/clean data.png) 


###Steps taken each day

![plot of chunk Plot histogram](figure/Plot histogram.png) 



####Mean and Median of steps per day per month




```
##    MeanOct MedianOct
## 2    63.00      63.0
## 3   140.15      61.0
## 4   121.16      56.5
## 5   154.58      66.0
## 6   145.47      67.0
## 7   101.99      52.5
## 9   134.85      48.0
## 10   95.19      56.5
## 11  137.39      35.0
## 12  156.59      46.0
## 13  119.48      45.5
## 14  160.62      60.5
## 15  131.68      54.0
## 16  157.12      64.0
## 17  152.86      61.5
## 18  152.36      52.5
## 19  127.19      74.0
## 20  125.24      49.0
## 21   96.93      48.0
## 22  154.71      52.0
## 23  101.34      56.0
## 24  104.44      51.5
## 25   56.64      35.0
## 26   77.02      36.5
## 27  134.92      72.0
## 28  110.17      61.0
## 29   80.94      54.5
## 30  110.33      40.0
## 31  179.23      83.5
```

```
##    MeanNov MedianNov
## 2   143.24      55.5
## 3   117.46      59.0
## 5   141.07      66.0
## 6   100.41      52.0
## 7   135.61      58.0
## 8    61.90      42.5
## 11  132.72      55.0
## 12  156.01      42.0
## 13   90.57      57.0
## 15   20.50      20.5
## 16   89.20      43.0
## 17  183.83      65.5
## 18  162.47      80.0
## 19  117.88      34.0
## 20   95.15      58.0
## 21  188.04      55.0
## 22  177.63      65.0
## 23  252.31     113.0
## 24  176.56      65.5
## 25  140.88      84.0
## 26  128.30      53.0
## 27  158.67      57.0
## 28  212.15      70.0
## 29  110.11      44.5
```



###Daily activity pattern (5 min intervals)   



![plot of chunk plot time interval](figure/plot time interval.png) 


####The maximum daily activity pattern   

The maximum daily activity is 835 at 0.3576  


###Addressing missing Values    
2304 rows have "na" values.






####Plot of 'Step' mean values with no missing value  
![plot of chunk plot mean ](figure/plot mean .png) 

####Plot of 'Step' mean values with  no missing value in 5 min intervale   
![plot of chunk median ](figure/median .png) 


###Plot of 'Step' mean values for weekdays in 5 min intervale

![plot of chunk create weekdays factor](figure/create weekdays factor.png) 
