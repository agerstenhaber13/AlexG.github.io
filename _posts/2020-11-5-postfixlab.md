---
layout: post
title: Postfix Lab

---

### Results
The average of all 100 lines in the dataset is **529.91**

### Stack Implementation
The stack is implemented in the evaluate() method. In this method, each row in the dataset is converted to a list. Additionally, an empty stack is created for each row. With these two components, the method then loops through each list and adds every element that is a number to the stack. For each element in the list that is not a number, which is every instance of a +,-, or *, it will pop the two previous blocks in the stack and evaluate them according to what operater is being used. Then, it will take the result of that operation and push it back on to the stack. After looking through every element in the corresponding list, the stack will only contain the final result of the postfix calculation. At this point, stack's peek() method is used to return the correct value.

### Process
For this lab, I spoke with Lucca about an issue with my subtraction calculation, but ended up fixing the issue on my own. In brainstorming how to approach this lab, I realized initially that I needed to turn each row in the dataset into a list. However, understanding how to implement the stack was more difficult. The two methods that I wrote, evaluate() and average() were the only methods that I tried, but I had many syntactical errors while writing them. One of these that really tripped me up was having to cast almost everything in evaluate to an int in order to do calculations. This lab really tought me how to think creatively about how to use stacks as well as how to work with the return types of methods.