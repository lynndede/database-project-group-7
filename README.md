Project Report: Flood Risk Management Database

PROJECT IDEA DEFINITION

The Flood Risk Management Database aligns closely with Sustainable Development Goal (SDG) 13: Where the goal of climate action is to counteract the effects of climate change.

SPECIFIC OBJECTIVES:

1.To monitor flood-prone areas
2.Track early warning systems
3.coordinate disaster response efforts.

KEY FUNCTIONALITIES 

1.Data Collection and Integration
2.Flood Monitoring
3.Warning systems(Continuously monitor weather conditions and water levels)
4.Disaster response

MAIN STAKEHOLDERS:

1.Local Governments
2.Emergency Services(Fire and Rescue Services)
3.Government departments(Meteorological Departments).
4.Non-Governmental organisations

HOW THIS PROJECT ADDRESS THEIR NEEDS:

1.May use the data for maintaining and improving flood defenses and drainage systems. 
2.Access real-time flood data to plan and execute rescue operations.
3.Where it will provide weather data and use the database for forecasting and early warning systems.
4.Health services can respond to health emergencies caused by flooding

Entities and Attributes

1.	Sensor refers to a device that gathers information  about environmental factors associated with possible floods
•	Attributes:
o	Sensor ID(Primary Key)
o	Location
o	Type (Rainfall , Water Level , Temperature)
o	Status (Active, Inactive) Flood Warning

2.  Warning ,based on data analysis,is an alert that notifies the appropriate stakeholders about the possibility of flooding.
•	Attributes: 
o	Warning ID (Primary Key)
o	Sensor ID (Foreign Key)
o	Warning Level (Low, Medium, High)
o	Timestamp

3. Response team refers to a group  of peopleor organiztions charged with organising relief activities and responding to crises like floods
•	Attributes:
o	Team ID (Primary Key)
o	Name
o	Contact details
o	Location

4.	Resource meaning the materials and equipment needed for disaster relief operations 
•	Attributes:
o	Resource ID (Primary Key)
o	Type (Medical, Food, Shelter)
o	Quantity
o	Location

5.	 Deployment is the process of installing, configuring, and allocating the components or resources required to efficiently coordinate response activities and monitor flood-prone areas
•	Attributes:
o	Deployment  ID (Primary Key)
o	Team ID (Foreign Key)
o	Resource ID (Foreign Key)
o	Timestamp
o	Status (Dispatched, En Route, Deployed, Completed)


Relationships
1.	Sensor to Flood Warning
•Type:	One to many relationship meaning that one sensor entity is related to many instances of flood warning entity
•	Cardinality: A single Sensor can generate multiple Flood Warnings
•	Participation: Each Floodwarning  must be associated with one Sensor entity.

2.	Response Team to Deployment:
•	Type: One-to-Many relationship meaning that one response team can be related to many deployment entities
•	Cardinality: A Response Team can have many  Deployments.
•	Participation: Each Deployment must be associated with one ResponseTeam.

3.	Resource to Deployment:
•	Type: One-to-Many relationship in that one resource entity can be related to many instances of deployment entities
•	Cardinality: A single Resource can be deployed many times.
•	Participation: Each Deployment must be associated with one Resource.

