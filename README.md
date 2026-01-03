📘 HR Data Analysis Project
Python
pandas
numpy
PowerBI
📂 Overview
This repository contains scripts and workflows for HR data analysis. The project focuses on:
- Cleaning and preprocessing HR datasets
- Parsing and standardizing date formats
- Converting textual numbers into integers
- Preparing data for visualization and reporting
The goal is to make HR data ready for insights in tools like Power BI, Tableau, or Python visualization libraries.

⚙️ Installation
Clone the repository:
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>


Install dependencies:
pip install -r requirements.txt


Or manually:
pip install pandas numpy python-dateutil word2number



📜 Usage
Import the required libraries:
import pandas as pd
import numpy as np
from dateutil import parser
from word2number import w2n


Example workflow:
# Load HR dataset
df = pd.read_csv("HRDataset.csv")

# Parse date column
df['DateofHire'] = df['DateofHire'].apply(parser.parse)

# Convert textual numbers to integers
df['Experience'] = df['Experience'].apply(
    lambda x: w2n.word_to_num(x) if isinstance(x, str) else x
)



📊 Features
- ✅ Data cleaning and preprocessing
- ✅ Date parsing and formatting
- ✅ Conversion of textual numbers to numeric values
- ✅ Ready for visualization in BI tools

📁 Project Structure
├── HRDataset.csv          # Sample HR dataset
├── analysis.ipynb         # Jupyter Notebook with workflow
├── requirements.txt       # Dependencies
└── README.md              # Project documentation






Would you like me to also make a professional GitHub profile-style README (with badges, stats, and a personal intro) so recruiters see both your project and your skills at a glance?
