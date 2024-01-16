# Data Visualization 300L Final Project

## Overview

This project is part of the Data Visualization 300L course, focusing on using Python for creating effective visualizations. The primary tools used are the Anaconda Integrated Development Environment (IDE) and Jupyter Notebook. The project leverages the power of Python libraries such as Pandas and Plotly to process and visualize data, enabling users to gain insights from complex datasets.

## Main Project: Employment Rates Visualization

### Project Structure

- **Final Project Folder**: Contains all the code and datasets used in this project.

### Technologies Used

- **Anaconda**: An open-source distribution of Python, ideal for data science and machine learning projects.
- **Jupyter Notebook**: A web-based interactive computing platform that allows the creation and sharing of documents containing live code, equations, visualizations, and narrative text.
- **Pandas**: A Python library providing high-performance, easy-to-use data structures and data analysis tools.
- **Plotly**: A graphing library that makes interactive, publication-quality graphs online.

### Code Explanation

#### 1. Choropleth Map of Employment Rates

```python
import pandas as pd
import plotly.express as px

# Load data
population_data = pd.read_csv('path_to_dataset.csv')

# Create a choropleth map
fig = px.choropleth(
    population_data,
    locations='LOCATION',
    color='Value',
    animation_frame='TIME',
    range_color=[0, population_data['Value'].max()],
    hover_name='LOCATION',
    hover_data={'Value': ':.2f'},
    title='Employment Rates by Country'
)
fig.show()
Purpose: Generates an interactive choropleth map displaying employment rates by country.
Data Source: CSV file containing employment data with columns 'LOCATION', 'Value', and 'TIME'.
Key Features: Uses Plotly Express to create a choropleth map, with dynamic range coloring and hoverable information.
2. Comparative Line Plots for Top and Bottom Countries
python
Copy code
import pandas as pd
import plotly.graph_objs as go
from plotly.subplots import make_subplots

# Load data
df
= pd.read_csv('UnemploymentRate7.csv')

Initialize subplots
fig = make_subplots(rows=3, cols=3, shared_xaxes=True, shared_yaxes=True)

Process and plot data for each country
... (detailed processing and plotting steps)
Finalize and display the plot
fig.show()

vbnet
Copy code

- **Purpose**: Creates a set of subplots comparing the employment rates of different countries.
- **Data Source**: Two CSV files, 'UnemploymentRate7.csv' and 'UnemploymentRatebottom7.csv'.
- **Key Features**: This script uses Plotly's graph objects and subplots to create a detailed comparison of employment rates across various countries. The data is read from two separate CSV files, each representing a group of countries (top and bottom in terms of employment rates). Each country's data is plotted as a line graph within a subplot, with a unique color assigned for clarity. Additionally, data for the OECD average is included for reference in each subplot. The layout is updated to include titles and a legend, ensuring the visualization is informative and easy to understand.

### Running the Code

To run these scripts:
1. Ensure that Anaconda and Jupyter Notebook are installed and set up on your system.
2. Open the Jupyter Notebook in the Final Project folder.
3. Run each cell of the notebook to execute the scripts and visualize the data.

### Conclusion

This project demonstrates the application of Python in data visualization, particularly in the field of employment rates analysis. The use of libraries like Pandas and Plotly provides a powerful toolkit for handling large datasets and creating dynamic, interactive visualizations that can aid in data-driven decision-making.

---
