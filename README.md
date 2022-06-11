# EXP. NO: 06

# DATE: 
# <p align = "center"> Poisson Process </p>


# Aim : 
To find the probability of that  (i) exactly 4 customers arrive (ii) more than 4 customers arrive (iii) fewer than 4 customers in 2 minute  arrival. Given that the customers arrive at a bank according to a Poisson process with mean rate of 3 per minute  during a time interval of 2 min. 


# Software required :  

Python

# Theory:

The Poisson process is one of the most widely-used counting processes. It is usually used in scenarios where we are counting the occurrences of certain events that appear to happen at a certain rate, but completely at random (without a certain structure). For example, suppose that from historical data, we know that earthquakes occur in a certain area with a rate of 2 per month. Other than this information, the timings of earthquakes seem to be completely random. Thus, we conclude that the Poisson process might be a good model for earthquakes. In practice, the Poisson process or its extensions have been used to model.

1. The number of car accidents at a site or in an area
2. The location of users in a wireless network
3. The requests for individual documents on a web server

 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/171325180-eaf80506-545c-4f35-878a-1e95aa0e81e3.png)



# Program :
```python
"""
Developed by: VEERAPALLI JANITH
Reg no:212220230057
"""
import numpy as np
import math
mean=3
t=2
def poisson(n):
    sum=1
    for i in range(1,n+1):
         sum=sum*i 
    p=math.exp(-mean*t)*(mean*t)**n/sum
    return round(p,2) 
fq=poisson(4)
print("The Probability of getting exactly 4 customers arrive = ",fq)

sq=1-(poisson(4)+poisson(3)+poisson(2)+poisson(1)+poisson(0)) 
print("The Probability of getting more than 4 customers arrive = ",sq)
tq=(poisson(3)+poisson(2)+poisson(1)+poisson(0))
print("The Probability of getting fewer than 4 customers in 2 minute arrival = ",tq)
```

 

# Output : 
![Screenshot (279)](https://user-images.githubusercontent.com/75243072/172534244-fde6f6e2-fa16-4695-8ce3-33da4a75f237.png)

# Result :
Thus,the probability of given problem using poisson process is implemented.
