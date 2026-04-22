# iot_proj_01

so hellow guys i will try my best to help you understand our porject :>

1st afall our project is devided into 2 parts Hardware system and Software system :

# Hardware system (Data Acquisition):-
the work of our hardware system is to get data from the environment and present it in a format that it can be understood by other programming languages you know like data is alawys stored in a fromat for example arrays is one way to do excel sheets is another way to do it so basically what we gonna do we gonna utilise the sensors in our esp32 module and take those data values and make a table out of them :

| Time       | Temp| sulight level | growth derivative |
|------------|-----|---------------|------------------ |
| 11:00 am   | 25  |     20        |    postive        |
| 12:00 am   | 30  |     30        |    postive        |  
| 01:00 am   | 22  |     40        |    negative       |

something kinda of like this then we will use a wifi module connected to our esp32 to send this table information to our computer system then hardawre part is over 

so our workflow kinda look like this :

...

Controller: ESP32 Module.

Sensors: Integrated sensors to monitor light levels, temperature, and moisture.

Data Formatting: Raw sensor data is structured into a readable format (similar to an array or CSV) for processing.

Communication: Data is transmitted from the ESP32 to a central computer system via Wi-Fi.

...

# Software system (Analysis & Visualization) :-
what we have recived is data of environment and its reactance to growth of plant for diffrent conditions plant will have diffrent growth what we want is to maxmise its growth so what we will do is to judge this data create a loss function like suitable oxgen level is 45 and we have recived that it is 40 so the loss in oxegen level is calculated to be 5 which is holding plant growth back if we can fulfill that loss we will have better plant growth 
so manually calculating loss and checking things is very hideous so what we gonna do is we gonna use the linear reggission model which automaticcally calculates what is best conditions for the plant treat it like a mathmatical function which takes some values and returns the values with maximum output that is about working of the system 

# 1. Predictive Analysis (Linear Regression)
Instead of manually checking if a plant has enough light or oxygen, we use a Linear Regression model.
Loss Function: The system calculates the "loss" (the gap between current conditions and ideal conditions).
Optimization: The model treats environmental factors as a mathematical function to determine which specific values will yield the maximum output for plant health.

...
# 2. Data Visualization

but we also need to show the progress of our system by visualsing all the data values about plant growth and environment so for that we are gonna use matplotlib library in python to plot all the data we have recived and for showing the user these graph thatt we have made we will be using cloud servers where a website will take the data and show the graphs to the user 

This generates visual graphs that represent:

Fluctuations in environmental data.
The correlation between specific conditions and growth rates.

# Tech Stack
Hardware: ESP32, Various IoT Sensors.

Language: C++ (for ESP32), Python (for Data Science).

Libraries: Matplotlib, Scikit-learn (Linear Regression), NumPy.

Platform: Cloud-based Web Dashboard.

# there are somelinks i would like to provide for better understanding of things 
esp32 intro - https://lastminuteengineers.com/getting-started-with-esp32/

dataLoading in esp32 - https://randomnerdtutorials.com/esp32-how-to-log-data/

official doc of our ml model - https://scikit-learn.org/stable/modules/linear_model.html 

for data visulazition model - https://matplotlib.org/stable/users/explain/quick_start.html
