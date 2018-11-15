U.S. Gasoline Production
========================================================
author: Team VP
date: November 30th, 2018
autosize: true


The Data
========================================================

U.S. Energy Information Administration  
Weekly U.S Product Supplied of Finished Motor Gasoline  
<https://www.eia.gov/dnav/pet/hist/LeafHandler.ashx?n=pet&s=wgfupus2&f=w>

- Time Series - Weekly data points from 2/8/1991 to current

- Dependent Variable - Average barrels per day (thousands)

- Created exogenous variable dataset with dummy variables for each season

Data Subsets
========================================================
For forecasting purposes, we will be looking at the last 260 weeks (~5 years)

- Training set (.tr) - Week 1 through week 206 (~3 years)

- Test set (.val) - Remaining 52 weeks (final ~1 year)


Data Variations and Frequencies
========================================================
Created three variations of data:  
______

oil_round:  
frequency = 52  
start oil_round.tr = (2013, 46)  
end oil_round.val = (2018, 45)  

*******
oil_freq:   
frequency = $365.25 / 7$  
start oil_round.tr =   
end oil_round.val =   

*******
oil_freq:   
frequency = $365.25 / 7$, $(365.25/7)/12$ 
start oil_round.tr =   
end oil_round.val =  



Slide With Code
========================================================


```r
summary(cars)
```

```
     speed           dist       
 Min.   : 4.0   Min.   :  2.00  
 1st Qu.:12.0   1st Qu.: 26.00  
 Median :15.0   Median : 36.00  
 Mean   :15.4   Mean   : 42.98  
 3rd Qu.:19.0   3rd Qu.: 56.00  
 Max.   :25.0   Max.   :120.00  
```

Slide With Plot
========================================================

![plot of chunk unnamed-chunk-2](forecastproj-figure/unnamed-chunk-2-1.png)