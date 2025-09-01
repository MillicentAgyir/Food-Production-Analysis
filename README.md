<<<<<<< HEAD
#  Transborder Freight Analysis Project

This project analyzes transborder freight data between the U.S., Canada, and Mexico to uncover trends, inefficiencies, and insights across transport modes, commodities, trade partners, and corridors. It applies data science techniques to inform infrastructure planning, trade strategy, and policy decisions.

---

##  Project Objectives

- Analyze freight movement patterns by transport mode, region, commodity, and time.
- Identify operational inefficiencies and cost anomalies.
- Assess environmental and safety-related impacts.
- Evaluate the effects of external shocks (e.g., policy changes).
- Provide actionable recommendations for stakeholders.

---

##  Business Questions

1. **What are the dominant transport modes (road, rail, air, water) over time, and how do their freight volumes compare annually and monthly?**  
   - 1.1. How does the distribution of freight volume vary by commodity type over time and mode?  
   - 1.2. Which origin-destination (OD) pairs or corridors have the highest freight movement, and how have they changed over time?

2. **Which commodities contribute the most to freight value and volume across different modes and trade partners (US, Canada, Mexico)?**

3. **Which origin-destination (OD) corridors or regions handle the largest freight volumes, and how have these patterns changed over time?**

4. **Are there inefficiencies or cost anomalies in freight transport, such as unusually high freight charges relative to shipment weight or value?**

5. **Which commodities have seen the most growth or decline in freight volume or value in the past 5 years?**

---


## 🔗 Data Access

The cleaned datasets used in this project are hosted on Google Drive.  
 [**Click here to access the data**](https://drive.google.com/drive/folders/1GrS6TwpOqdmMyVTh6MO642YxO4y1Peqm?usp=sharing)  


Download the files and place them in the `data/` directoryroot of the project folder before running any notebooks.

---

##  Setup Instructions

### 1. Clone the repository


git clone https://github.com/your-username/transborder-freight-analysis.git
cd transborder-freight-analysis

### 2. Create a virtual environment

python -m venv env
# Activate the environment
source env/bin/activate        # On Mac/Linux
env\Scripts\activate           # On Windows

### 3. Install dependencies

pip install -r requirements.txt

### 4. Download the data
Use the Google Drive link to download the datasets.

## Project Workflow

Step 1: Data Understanding
Loaded .csv data chunks from deduped files.

Reviewed features like MODE, SHIPWT, COMMODITY2, VALUE.

Identified trends and inconsistencies.

Step 2: Data Cleaning
- Removed nulls and filled relevant columns.

- Converted data types, deduplicated entries.

- Validated row counts per chunk.

Step 3: Exploratory Data Analysis (EDA)
Aggregated yearly and monthly shipment volumes.

Compared freight volume by mode.

Analyzed commodity distribution across countries.

Step 4: Business Questions Answered
Q1: Dominant Transport Modes & OD Corridors

Q2: Top Commodities by Value & Volume

Q3: Largest Freight Corridors

Q4: Freight Inefficiencies

Q5: Growth/Decline in Commodities

Tools & Technologies
Python (pandas, seaborn, matplotlib)

Jupyter Notebooks

Google Drive (Data Storage)

Git & GitHub (Version Control)



 ## Dependencies
This project uses the following Python libraries:

pandas

numpy

matplotlib

seaborn

plotly 

All dependencies are listed in requirements.txt.

🙋‍♀️ Contributors
Feel free to fork, submit pull requests, or create issues to suggest improvements.

📬 Contact
For questions or feedback, please reach out via:
📧 agyirnanagmail.com







=======
#  Transborder Freight Analysis Project

This project analyzes transborder freight data between the U.S., Canada, and Mexico to uncover trends, inefficiencies, and insights across transport modes, commodities, trade partners, and corridors. It applies data science techniques to inform infrastructure planning, trade strategy, and policy decisions.

---

##  Project Objectives

- Analyze freight movement patterns by transport mode, region, commodity, and time.
- Identify operational inefficiencies and cost anomalies.
- Assess environmental and safety-related impacts.
- Evaluate the effects of external shocks (e.g., policy changes).
- Provide actionable recommendations for stakeholders.

---

##  Business Questions

1. **What are the dominant transport modes (road, rail, air, water) over time, and how do their freight volumes compare annually and monthly?**  
   - 1.1. How does the distribution of freight volume vary by commodity type over time and mode?  
   - 1.2. Which origin-destination (OD) pairs or corridors have the highest freight movement, and how have they changed over time?

2. **Which commodities contribute the most to freight value and volume across different trade partners (US, Canada, Mexico)?**

3. **Which origin-destination (OD) corridors or regions handle the largest freight volumes, and how have these patterns changed over time?**

4. **Are there inefficiencies or cost anomalies in freight transport, such as unusually high freight charges relative to shipment weight or value?**

5. **Which commodities have seen the most growth or decline in freight volume or value in the past 5 years?**

---


## 🔗 Data Access

The cleaned datasets used in this project are hosted on Google Drive.  
 [**Click here to access the data**](https://drive.google.com/drive/folders/1GrS6TwpOqdmMyVTh6MO642YxO4y1Peqm?usp=sharing)  


Download the files and place them in the `data/` directoryroot of the project folder before running any notebooks.

---

##  Setup Instructions

### 1. Clone the repository


git clone https://github.com/your-username/transborder-freight-analysis.git
cd transborder-freight-analysis

### 2. Create a virtual environment

python -m venv env
# Activate the environment
source env/bin/activate        # On Mac/Linux
env\Scripts\activate           # On Windows

### 3. Install dependencies

pip install -r requirements.txt

### 4. Download the data
Use the Google Drive link to download the datasets.

## Project Workflow

Step 1: Data Understanding
Loaded .csv data chunks from deduped files.

Reviewed features like MODE, SHIPWT, COMMODITY2, VALUE.

Identified trends and inconsistencies.

Step 2: Data Cleaning
- Removed nulls and filled relevant columns.

- Converted data types, deduplicated entries.

- Validated row counts per chunk.

Step 3: Exploratory Data Analysis (EDA)
Aggregated yearly and monthly shipment volumes.

Compared freight volume by mode.

Analyzed commodity distribution across countries.

Step 4: Business Questions Answered

Q1: Dominant Transport Modes & OD Corridors

Q2: Top Commodities by Value & Volume

Q3: Largest Freight Corridors

Q4: Freight Inefficiencies

Q5: Growth/Decline in Commodities

Tools & Technologies
Python (pandas, seaborn, matplotlib)

Jupyter Notebooks

Google Drive (Data Storage)

Git & GitHub (Version Control)



 ## Dependencies
This project uses the following Python libraries:

pandas

numpy

matplotlib

seaborn

plotly 

All dependencies are listed in requirements.txt.

🙋‍♀️ Contributors
Feel free to fork, submit pull requests, or create issues to suggest improvements.

📬 Contact
For questions or feedback, please reach out via:
📧 agyirnana@gmail.com









>>>>>>> 858f908389f6061b9d0c14893b46110d1ae084ad
