---
layout: post
title: Hospital Lab

---

### Conclusion
The county with the most hospital beds per person, regardless of type, was the city of New York. It had roughly 7.14 hospital beds per person.

### Getting and Cleaning the Dataset
In order to get the first version of the dataset, I recycled much of the code that we used for the weather API and applied it to the hospital API. The changes that I had to make involved altering the url, key, and endpoint for the new API as well as writing a method called allValues() to print all the obtained values. This method only prints lines as long as the API returns actual values for locations. 

I wrote two different methods to clean the data, but only used one of them for the purposes of this lab. I used 1000HAB as the standard for both. The first was the clean() method, which simply prints out a cleaned version of the inputed csv with adjusted measure and bed values. This data could then be piped and made into a new, cleaned csv, but this wasn't as efficient for my purposes and was simply the first method I tried.

The second method, total(), which also takes the uncleaned csv file as an input, totals the hospital bed per capita data for every location, regardless of type, adjusting for the changes in measurement. At the end of this method, I simply print out a dictionary with all of the locations only represented once, their total hospital beds per capita, and the county with the most beds per capita and how many beds it has. Writing this method saved me the step of analyzing a cleaned dataset by simply cleaning the data as I analyze it. 

### Process

For this lab, I collaborated heavily with David, Alexis, Ethan, and Lucca while trying to troubleshoot the getBeds method so that it returned the right data. The issue came primarily with only printing the first line because of the way I wrote the lines that check if there is still data to be retrieved. After that, I worked on this lab entirely on my own on the cleanthebeds file, which contains the mehtods I used to clean and analyze the data. The process of working on this file was relatively smooth-sailing as most of my issues were simple syntactical ones that didn't cause me too much trouble. These issues mostly portained to the use of different datatypes such as string and float when either retrieving data from the csv file or calculating different values using that data to adjust for differences in measurement. 