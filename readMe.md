 # Introduction
 The proposed intrusion detection system's (IDS) description.
 This solution uses an advanced ML technique to identifly and classity harmful behaviour in The systems 
 goal was to create a real-time intrusion dete ction system that would assist organization systems in detecting these
 abnormalities in realtime and in aiding these organizations in resolving the anomalies before they compromise sensitive data
 and cause losses in revenue.
 
 The Dataset is gotten from honeypot
 
 
# Three modules 

### Data Gathering:
In order to achieve this research goal, I first created a virtual machine on AWS and attached a honeypot to it. The honeypot was used to collect data from the attackers which was used for further analysis.

### Data Visualizations:
Kibana was attarched to the Honeypot for realtime visulaizations of the attarck density.

Kibana is a data visualization and exploration tool used for log and time-series analytics, application monitoring, and operational intelligence use cases. It offers powerful and easy-to-use features such as histograms, line graphs, pie charts, heat maps, and built-in geospatial support.

### Data Processing:
After 14days of running the instance, I was able to gather 359,696 attark logs, export it from the dockerized honeypot to the home storage of the EC2 instance and finally to my local system to carry out the following:
1. Data clearning
I cleaned and merged 132 logs which was over 200,000 and after cleaning and reduced/resulted to 6,794
I attarched a notebook (honey_pot_DA) where i perform the Data Analysis.

2. Feature Engineering
The features with a lot of Nan values were dropped of and also some other feature which will have no effect/impact in the performance of the machine learning model.
the feature used includes:

Source IP(src_ip):  
the IP packet field containing the IP address of the workstation from which it came.

Destination IP(dest_ip): 
The IP packet field containing the IP address of the workstation to which it is addressed

Source_port : 
A source port is the TCP or UDP number used by a program to send data to another program on one end

destination port:
A destination port is the TCP or UDP number used by a program on one side of communication to receive data from another program on the other end.

protocol:
an established set of rules that determine how data is transmitted between different devices in the same network. Essentially, it allows connected devices to communicate with each other, regardless of any differences in their internal processes, structure or design

Class: 
the class of attark, it is also our target variable.

3. Modelling: building the Intrusion Detection Based Machine Learning MOdel(IDS).


### Modelling:

