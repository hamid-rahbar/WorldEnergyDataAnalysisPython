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
  

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.1.Jpg">Correlation Matrix 1<img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.1.Jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.2.Jpg">Correlation Matrix 2<img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.2.Jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.3.jpg">Scatter Plot<img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.6.1.3.jpg"></a> <br>
 
    
<p>    
<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights based on Correlation:}$<br>
            1. According to the correlation matrix, the primary energy consumption in G7 countries is primarily electricity:<br>
            &nbsp&nbsp&nbsp&nbsp * There is a strong correlation between energy consumption and both electricity demand and generation.<br>
            2. It is noteworthy that even though electricity constitutes the majority of the primary energy consumption in G7 countries, they do not necessarily prioritize generating it themselves to meet demand:<br>     
            &nbsp&nbsp&nbsp&nbsp * The proportion of electricity in total energy consumption is not necessarily correlated to electricity generation.<br>
            3. The G7 prefers electricity import rather than generating it from Nuclear source: <br>
             &nbsp&nbsp&nbsp&nbsp * The nuclear generation is negatively correlated with the electricity import.<br>
            3. Further investigation is required to gain deeper insights into these observations, which will be conducted in subsequent sections of the report. <br>
    </span>  
</div>
</p>

<a id="Modeling"></a>
<h2>   
    <font color = blue>
        <span>
            7. Data Modeling and Analysis
        </span>   
    </font>    
</h2>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.1.jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.2.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.2.jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.3.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.3.jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.4.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.1.4.jpg"></a> <br>

<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights:}$<br>
            1. Canada has a high energy and electricity consumption per capita compared to other G7 countries.<br>
            2. Electricity is widely considered to be a clean energy source due to its low emissions and pollution levels. As the world shifts towards more sustainable energy solutions, the use of electricity has become increasingly popular. In particular, among the G7 countries, the share of electricity in their total energy consumption has been on the rise, especially in France and Japan. These countries have made significant investments in renewable energy sources such as wind, solar, and hydro power, which has helped increase the share of electricity in their energy mix. This trend towards cleaner energy sources is expected to continue as countries work towards reducing their carbon footprint and meeting international climate goals.<br>
            3. Italy is among the largest importers of electricity among the G7 countries, relying heavily on foreign sources to meet its energy needs. On the other hand, France, Canada, and Germany are significant exporters of electricity, with France ranking as the top exporter among the G7 countries. These countries have established themselves as major players in the global energy market, leveraging their abundant natural resources, and modern energy infrastructure. However, Japan stands out as a unique case among the G7 countries, with no imports or exports of electricity. This is due to the country's focus on energy self-sufficiency, which is achieved through a combination of energy efficiency measures and investments in its own energy infrastructure, including nuclear power and renewable energy sources. These diverse energy dynamics among the G7 countries highlight the importance of energy trade and cooperation in the global energy market. <br>
    </span>  
</div>
