###NSS Capstone: Roadway Network Analysis

### Overview
This presentation investigates the root causes of roadway accidents on the East End Crossing project and pinpoints the roadside assets that are struck most often.

The goal is to guide proactive stocking, targeted maintenance, and low-cost safety counter measures.

###Key Questions
1. Primary Question: Are vehicle crashes within the project’s right-of-way correlated with any of the following factors? Low pavement friction levels, changing traffic volumes, specific times of the day or days of the week, weather conditions, etc.
2. Which assets are most commonly struck and required higher stocking?

###Technologies Used
The project is presented in Power BI using a variety of visualizations that include maps, slicers, bar charts, matrix tables, etc. Cross-report relationships are common among many of these tools and Canva was used on one slide as well. 

In addition to Power BI, Python was utilized to create an interactive map for analysis. The map shows the friction data from various years with annual crash locations similarly layered on top. Each crash is represented by a black dot; hovering over a specific dot displays useful information such as collision date, time, primary factors leading to the crash, the manner in which the crash happened, the condition of the pavement surface and the weather at that time. The python map was replicated in the presentation using a Microsoft Azure map.

Finally, all data was cleaned, reviewed and otherwise managed in Microsoft Excel. These files can be found in the GitHub associated with this presentation.

###Interacting with Project Tools
The Power BI file titled “ABH Capstone_Roadway Analysis” is the primary platform the presentation should be viewed. If the user would like additional flexibility in their exploration, they can open the html file called “crash_friction_map”. Should there be interest in reviewing the code supporting this html file it has been included as “Roadway Analysis_Final”.

###Data Sources
Data was acquired from three entities. These entities are as follows:

- Friction data is produced annually from a consultant, Applied Research Associates (ARA), at the request of East End Crossing Partners. 
- Crash information was received from the Indiana Department of Transportation (INDOT). INDOT is one of many stakeholders and the client representative for the project. 
- Information related to damaged assets was produced internally from East End Crossing Partner’s asset management system. 
- Traffic counts were also produced internally by East End Crossing Partners

##Datasets
- Accidents.xlsx \ This is the primary dataset utilized for this project. This information was provided by INDOT.
- Assets Damaged.xlsx \ Data produced internally that details which asset catagories are damaged most often.
- Causes.xlsx \ A subset of the accidents file that details the nature of the crashes.
- crash_friction_map.html \ A map created with python that was used for intial analysis
- Date.xlsx \ A subset of the accidents file that contains all information related to crash dates and time
- friction_data.xlsx \ The dataset from ARA that contains the friction values
- Location.xlsx \ A subset of the accidents file that details where crashes occurred
- Time of day.xlsx \ An ad-hoc file for analysing the time of day crashes occurred
- traffic_counts.xlsx \ Data produced internally that tracks annual traffic counts
- ABH Capstone_Roadway Analysis.pbix \ Final capstone Power BI file
- Roadway Analysis_Final.ipynb \ Python code supporting the html file

###Methodology
The primary accident dataset included thousands of records that were outside of the project limits. To filter the data to only those pertinent to this presentation, I utilized a third-party online service, kepler.gl. Using this program, I imported a CSV file containing the master record number unique to each crash, the crash latitude and longitude and a separate GeoJSON file containing the project limits. The GeoJSON was then used as a filter on the crash file and exported giving me the crash location and unique identifier for the East End Crossing project. With the master record number, an xlookup was used to filter the complete accident dataset. 

The Assets Damaged file necessitated removing several fields not required for this project. Otherwise, the remaining excel files are subsets of accidents.xlsx with some calculated fields included. Among those calculated fields are the Driver Related and Behavior Category in Causes.xlsx. These are each derivative of the Primary Factor behind the crashes that helped drill down the presentation to aggressive driving at the ramps.

The python map was produced in Jupyter Notebooks. It was coded using proprietary knowledge gained in the NSS bootcamp as well as online sources. The primary external sources are as follows:
- A Look at Folium. Folium is a feature rich library used…   by Christos Maglaras   Analytics Vidhya   Medium
- Circle and CircleMarker — Folium 0.20.0 documentation
- Creating Interactive Geospatial Maps in Python with Folium – Water Programming  A Collaborative Research Blog
- FeatureGroup is checked or not Folium Map Python - Stack Overflow
- Folium Geospatial Data Visualization Tutorial
- Python Folium  Create Web Maps From Your Data – Real Python

###Contact
Andy Huber
abhube2@gmail.com
linkedin.com/in/andy-huber-pe-285b1114

