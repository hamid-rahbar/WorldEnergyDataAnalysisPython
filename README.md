# World Energy Data Analysis (1900-2020)
### <a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/World.Energy.Data.Analysis.Non.Interactive.ipynb">Python Code in Jupiter Notebook</a>
In this project, I utilize different Python packages, including:
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Geopandas
- Folium
- Ipywidgets

<h2>   
    <font color = blue >
        <span style='font-family:Georgia'>
            Table of Contents:
        </span>   
    </font>    
</h2>
<span style='font-family:Georgia'>
    <ol>
        <li><a href='#TypesOfEnergy'>Types of Energy</a></li>
        <li><a href='#GetReady'>Getting Jupyter Ready</a></li>
        <li><a href='#Importing'>Reading and Understanding the data</a></li>
        <li><a href='#Assumptions'>Assumptions</a></li>
        <li><a href='#Objectives'>Objectives</a></li>
        <li><a href='#Cleaning'>Data Cleaning and Manipulation</a></li>
        <li><a href='#Modeling'>Data Modeling and Analysis</a></li>
        <li><a href='#Overview'>World Energy Overview</a></li>
</span>
  
<a id="TypesOfEnergy"></a>
<h2>   
    <font color = blue>
        <span>
            1. Types of Energy:
        </span>   
    </font>    
</h2>
    
Energy generation and consumption can be categorized as follows: <br>
- Fossil Energy: Coal, Oil, Gas, and Low-Carbon Fuels <br>
- Nuclear Energy <br>
- Renewable Energy: Hydro, Wind, Solar, Biofuel, and other Renewable Sources
  
<a id="GetReady"></a>
<h2>   
    <font color = blue>
        <span>
            2. Getting Jupyter Ready:
        </span>   
    </font>    
</h2>
Please refer to the <a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/World.Energy.Data.Analysis.Non.Interactive.ipynb">Jupyter Notebook</a> of the project. <br><br>
    
<a id="Importing"></a>
<h2>   
    <font color = blue>
        <span>
            3. Reading and Understanding the Data:
        </span>   
    </font>    
</h2>
Please refer to the <a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/World.Energy.Data.Analysis.Non.Interactive.ipynb">Jupyter Notebook</a> of the project. <br><br>
    
<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insight:}$<br>
        - The dataset consists of 21861 energy related data for 305 countries and regions from 1900 to 2021 in 129 fields.<br>
        - Column's type are object, int64, and float64 and it seems each field's type conform with its content, so there is no need for correction.<br>
        - However, there are some data that pertains to the continents. Additionally, some other data refers to names of regions or part of some continents that only the creator of the dataset can interpret. As a result, not all the data can be utilized and the data requires cleaning.<br>
    </span>  
</div>
 
<a id="Assumptions"></a>
<h2>   
    <font color = blue>
        <span>
            4. Assumptions:
        </span>   
    </font>    
</h2>
- The G7 countries considered for analysis in this report, including: United States, Canada, United Kingdom, France, Germany, Italy, and Japan.<br>
- The period of 31 years, from 1990 to 2021, also consider for the analysis.<br>
- Here is the link to the dataset source: <a href='https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/owid-energy-data.csv'> Click Here </a> <br>

<a id="Objectives"></a>
<h2>   
    <font color = blue>
        <span>
            5. Objectives:
        </span>   
    </font>    
</h2>    

The objective of this analysis is to answer the following questions: <br>
1. Which country consumes the most energy in the world?
2. What is the energy consumption per capita or per GDP for each country?
3. What is the percentage of energy consumption that is electricity?
4. How does the consumption of primary energy sources (fossil, nuclear, renewable) compare?
5. Which source of energy has grown the most over the last 30 years?
6. Energy production patterns in different countries, including the source of energy production, such as coal, gas, oil, or biofuels.
7. Energy consumption patterns in different countries, including per capita energy consumption, the share of energy consumption from different sources, and the change in energy consumption over time.
8. Energy production and consumption trends in different countries, including the annual change in energy production or consumption and the share of energy production or consumption in different energy sources.
9. The relationship between energy production, consumption, and economic indicators, such as GDP, population, and energy consumption per GDP.
10. The environmental impact of energy production and consumption, including greenhouse gas emissions and carbon intensity of electricity production.
    
    
<a id="Cleaning"></a>
<h2>   
    <font color = blue>
        <span>
            6. Data Cleaning and Manipulation
        </span>   
    </font>    
</h2>
    
<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.1.Jpg">Correlation Matrix 1<img align="left" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.1.Jpg"></a>
