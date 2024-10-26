Air pollution, both indoor and outdoor has become a concerning issue worldwide. Among the air 
pollutants Particulate Matter (PM) Carbon Dioxide (CO2) Carbon Monoxide (CO) Ground level 
Ozone (O3) Nitrogen Oxides (NOx) Sulfur Oxides (SOx) and Lead (Pb) are the significant ones 
found in our environment. This environmental health problem affects people, in both developing 
countries. 
When it comes to air pollution emissions from motor vehicles, fuel burning and industrial 
activities are the primary sources. In Sri Lanka 24,000 deaths were attributed to air pollution in 
2012 [1]. The respiratory health symptoms resulting from air pollution include lower respiratory 
tract infections, pneumonia, bronchitis, asthma, reduced lung functions and growth as well, as 
lung cancer [2]. In 2016 ambient (outdoor) air pollution was estimated to cause around 4.2 
million deaths globally in both urban and rural areas 
The primary source of air pollution, in Sri Lanka is the emissions from vehicles, which account for 
than 60% of the emissions in Colombo [4]. Considering the population in Sri Lanka school 
children are particularly vulnerable to levels of pollutants due to overcrowding in schools located 
in cities, especially Colombo and Kandy. The levels of air pollutants were significantly greater, 
within the premises of schools when compared to schools 

Sri Lanka is facing a serious air pollution problem that severely impacts the daily life of 
every Sri Lankan. The main source of ambient air pollution in Sri Lanka is vehicular 
emissions. A methodology to monitor the air quality in real-time with an overall coverage 
of Sri Lanka, and automatically process these huge data to identify air quality levels in a 
specific area is now becoming a timely research topic. 

An air quality monitoring and analysis based predictive system is proposed to monitor the 
ambient air quality, provides the best route with minimum polluted air, maps the 
heatmaps to identify the current air quality of an area easily and predict the future air 
quality of each area. The prototype was implemented by hierarchically deploying two 
different gas sensors, an Arduino Uno board and a Wi-Fi module, to implement in open 
spaces between smart buildings, and transfers the sensor data back to the information 
processing center by using IoT technology for real-time display. The information 
processing center stores real-time information which is collected from the sensors to the 
database. By reading sensor data stored in the database, the front-end system draws real
time, accurate air quality levels included maps and predicts the less polluted routes and 
the air quality level over an area.  

To address this problem, An innovative solution proposed for the above scenario would 
be a prototype which uses an air quality monitoring device and a mobile application to 
visualize air quality information in terms of route suggestions, heat map, and air quality 
predictions. People’s awareness is the main objective of this research, and it helps people 
who are suffering from respiratory diseases, kids and older persons to avoid the most 
polluted areas by identifying highly polluted areas when traveling. 

Pollution Levels Prediction: 
The primary objective of this component is to develop a robust model for predicting 
pollution levels. This involves analyzing historical data, current environmental conditions, 
and other relevant factors to forecast the concentration of pollutants in the air 
accurately. Through rigorous analysis, the project team pinpoints the variables with the 
most substantial impact. Subsequently, feature engineering techniques are applied to 
enhance the model's predictive capabilities. This involves transforming and manipulating 
the chosen features to extract more valuable information and improve the overall 
accuracy of the predictive model. The predictive model introduces dynamic predictions, 
a unique feature that enables real-time adjustments based on changing environmental 
factors. This innovation enhances the model's responsiveness to rapidly evolving 
conditions. Furthermore, the integration with the route generation component ensures 
that the pollution prediction model actively contributes to the generation of optimal and 
least-polluted paths. 
To further strengthen the system's transparency and user awareness, a comparison with 
real-time pollution data is implemented. This comparison serves not only for accuracy 
validation but also to showcase potential conflicts or deviations. A graphical 
representation is employed to illustrate the comparison between past, present, and 
future predicted data. The graph provides a visual narrative, allowing users to discern 
patterns, anomalies, and potential discrepancies between real-time observations and 
model predictions. This comprehensive approach enhances the system's credibility, 
providing users with a holistic understanding of the environmental dynamics and 
fostering greater trust in the predictive capabilities of the air quality monitoring system.

Sensor based device creation and value accuracy: 
In this component, MQ4, and MQ7 sensors were used to measure Methane (CH4) and 
Carbon Monoxide (CO) gases in the air respectively. The conductivity increases with the 
increment of gas concentration in the polluted air, when polluted air goes through these 
sensors. 

The difference of conductivity can be converted into gas concentration values, by 
implementing an Arduino code using the Arduino Uno board. The output analog value 
(0 - 4095) of each sensor should be converted into sensor voltage value using the (1). 
Sensor Voltage = (Analog Reading * 3.3V) / 4095 (1) 
After sensor voltage calculation, we can convert that value into a Parts per Million (PPM) 
concentration value using the sensitivity calibration curve of each gas sensor given in 
their datasheets separately, which were drawn under the standards between the two 
axis; the gas concentration (PPM) and sensor voltage (V). With the aid of those sensitivity 
curves of each gas sensor, built two relationships as (2) and (3) for the sensors separately, 
to convert the sensor voltages into concentration value. Using the graphical analysis 
software, Engauge Digitizer; points of these graphs were selected and drew an 
exponential to that graph using the selected points. With the aid of that drawn 
exponential, declared equations to each graph for building the relationship between 
sensor voltage and gas concentration in ppm. The equations built for the relationship of 
gas concentration (ppm) and sensor voltage (V_RL) of two sensors are as follows.  
 
 
The ESP8266 Wi-Fi module is used to transmit the sensor data to the database in every 
one minute of time interval to make the device more real in time. The location of the 
device is identified using a predefined terminal number to the places where the devices 
implemented. Instead of using a GPS system, this predefined terminal number system 
was used for reducing the size of the data packet, as this system is a more real-time 
system, and it uploads the data in every 1 minute of the time interval. This allocated 
terminal number is also uploaded with the sensor data for the ease of identification of 
device location.  
The data packet is sent by using a Hypertext Transfer Protocol (HTTP) Post request. The 
packet uses encoded format when sending to the server, to increase the security of the 
data packet. A Transmission Control Protocol (TCP) connection is established with the 
server by the Wi-Fi module. An Arduino Uno board is used to implement the data 
processing code. This Arduino code handles the sensors to get the sensor inputs, process 
them and handles the Wi-Fi module to send these processed outputs to the database. 
In addition to the aforementioned components, the designed hardware enhances user 
notification capabilities. Specifically, the hardware is equipped to send email 
notifications to registered email addresses whenever the sensor detects high readings 
for particulate matter or Carbon monoxide. This notification feature adds an extra layer 
of proactive communication, alerting users to potential environmental risks and 

Real-time pollution map: 
This component focuses on providing a visual representation of real-time pollution levels across 
different regions to facilitate informed decision-making. It is a graphical representation of data 
that uses a system of color-coding to represent different values. It used in various forms of 
analytics but is most commonly used to show user behavior on specific situation. There are two 
heat maps were generated for methane and carbon monoxide separately. It is generated using 
accurate sensor data stored in the database, JavaScript and HTML language. Latitude and 
longitude are related to the terminal number, which is used to identify the location. Then using 
color schemes, the sensor values related to the location are displayed separately in two maps. 
Moreover, it displays the real time level of air pollution in an area. Many different color schemes 
can be used to illustrate the heat maps. In the mobile application, users can use the heat maps 
to identify the air polluted in an area, due to high amounts of various gases in that area. 
In addition to its primary function of providing a visual representation of real-time pollution levels 
across different regions, this component incorporates cutting-edge technology to enhance user 
experience. Leveraging Natural Language Processing (NLP), a voice assistant has been integrated, 
allowing users to obtain information about areas with high pollution levels through spoken 
queries. Furthermore, language accessibility is prioritized with the implementation of a 
translator supporting both Tamil and English languages. This innovative approach not only 
empowers users to visually assess pollution data but also enables seamless interaction and 
understanding of the information using advanced language technologies. 
Real-time route generation is based on pollution: 
The aim of the sophisticated "Real-time route generation based on pollution" component is to 
provide users with the most optimal routes to their destinations. This cutting-edge system takes 
into consideration both the distance and air quality factors. To achieve this, an innovative 
algorithm, which combines Dijkstra's algorithm with a dynamic mapping process, is employed. By 
modifying Dijkstra's algorithm to include pollution levels, the system ensures that users 
commence their journeys from the closest non-polluted point, thereby minimizing their exposure 
to unhealthy air quality. In this process, gas concentration data, measured in Parts Per Million 
(PPM), plays a critical role, with color-coded interpretations indicating the severity of pollution. 
The algorithm analyzes real-time mapping data and gas concentrations to suggest routes that not 
only minimize distance but also prioritize areas with cleaner air. These suggested routes, which 
incorporate visual markers, such as red for starting points, blue for endpoints, and green for non
polluted areas, are then seamlessly integrated into a mobile application. This user-friendly 
interface enables individuals to input their desired destinations and receive visually represented 
routes that prioritize their health and safety. The solution is designed for real-life applications, 
providing users with a comprehensive travel experience that not only emphasizes efficiency but 
also takes into account the well-being of individuals by avoiding areas with high pollution levels. 
![img1](https://github.com/user-attachments/assets/78b833fb-0644-46a6-b255-3817dcce9bcd)
![img3](https://github.com/user-attachments/assets/e95cc76a-f831-4a17-b377-37657c911445)


https://github.com/user-attachments/assets/7f9e99ed-073b-4b48-9eb3-18e61c103831

