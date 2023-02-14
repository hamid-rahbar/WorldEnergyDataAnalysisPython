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

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.2.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.2.1.jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.3.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.3.1.jpg"></a> <br>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.3.2.png"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.3.2.png"></a> <br>

<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights:}$<br>
            1. The energy consumption patterns in the United States have experienced annual fluctuations over the last 10 years. This is true for both fossil and renewable energy sources, with shifts in consumption levels reflecting changes in the economy, energy prices, and government policies. Over this time period, the United States has experienced periods of increased energy consumption, as well as periods of reduced consumption during economic downturns. These fluctuations highlight the complex interplay between energy demand and economic conditions, as well as the ongoing transition towards a more sustainable energy mix. Despite the fluctuations, renewable energy sources have gained a greater share of the energy mix over the last few decades, reflecting the country's growing commitment to reducing its carbon footprint and increasing its use of clean energy sources. <br>
            2. The United States has experienced reductions in energy and electricity consumption in recent years, specifically in 2008, 2009, and 2020. The reductions in 2008 and 2009 were primarily driven by the global financial crisis and its impact on the economy, leading to a decrease in industrial activity and energy demand. In 2020, the reduction in energy consumption was largely due to the COVID-19 pandemic, which resulted in widespread lockdowns, reductions in travel and economic activity, and a decrease in energy demand. These reductions in energy consumption demonstrate the responsiveness of the energy system to changes in economic conditions and highlight the importance of energy efficiency measures in reducing overall energy demand. As the country looks to recover from the pandemic and address its long-term energy challenges, it will be important to consider both economic and environmental factors in shaping its energy policies and investments.<br>
            3. The other G7 countries are making efforts to reduce their dependence on nuclear energy and increase investment in renewable energy sources. This shift towards a cleaner energy mix reflects a growing recognition of the environmental and health risks associated with nuclear power, as well as the increasing competitiveness of renewable energy technologies. In particular, Japan stands out as a leader in this transition, with a significant reduction in its use of nuclear energy between 2010 and 2011. This reduction was a direct response to the Fukushima disaster in 2011, which raised concerns about the safety of nuclear power in the country and led to a shift towards alternative energy sources. These efforts towards reducing the use of nuclear energy and increasing investment in renewable energy demonstrate the commitment of G7 countries to creating a more sustainable and secure energy future.<br>
            4. Germany and the United Kingdom have both seen increases in the use of renewable energy in recent years. In Germany, the use of renewable energy sources grew rapidly between 2007 and 2017, reflecting the country's ambitious energy transition policies and its commitment to reducing its carbon footprint. This increase in renewable energy was driven by a combination of policy support, investments in renewable energy infrastructure, and advancements in renewable energy technologies. Similarly, the United Kingdom experienced a significant increase in the use of renewable energy between 2013 and 2020, reflecting the country's efforts to transition away from fossil fuels and towards a cleaner energy mix. This increase in renewable energy was driven by policy support, including government incentives and regulations, as well as the declining cost of renewable energy technologies. These trends demonstrate the progress that can be made in transitioning towards a more sustainable energy system and highlight the importance of continued investment and policy support in the renewable energy sector.<br>
    </span>  
</div>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.4.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.4.1.jpg"></a> <br>

<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights:}$<br>
            1. While the United States, the United Kingdom, Germany, Italy, and Japan are still heavily reliant on fossil fuels, both Canada and France have made notable progress in increasing their use of renewable energy. <br>
            2. Despite being primarily based on fossil fuels, Canada and France rank among the highest in renewable energy consumption among the G7 countries. This reflects their efforts to transition towards a cleaner energy mix and reduce their dependence on fossil fuels.  <br>
            3. Additionally, all of the G7 countries have started to reduce their reliance on nuclear energy, reflecting growing concerns about the environmental and health risks associated with nuclear power. These efforts towards reducing the use of fossil fuels and nuclear energy, and increasing investment in renewable energy, demonstrate the commitment of G7 countries to creating a more sustainable and secure energy future.<br>
    </span>  
</div>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.5.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.5.1.jpg"></a> <br>

<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights:}$<br>
            1. The energy mix for electricity production among the G7 countries varies greatly, with each country having its own unique approach to balancing its energy sources. <br>
            2. The United States has long been reliant on fossil fuels for electricity production, but has started to invest in renewable energy sources in recent years. <br>
            3. Meanwhile, Canada primarily relies on renewable energy sources for its electricity production.<br>
            4. The United Kingdom, Germany, and Italy have been successful in increasing their investment in renewable energy, resulting in a balance between electricity production from fossil and renewable sources.<br>
            5. France primarily relies on nuclear power for electricity production.<br>
            6. Japan continues to rely heavily on fossil fuels, with an increase in the use of fossil fuels for electricity production following a reduction in the use of nuclear energy. <br>
            7. These differences reflect the diverse energy needs, resources, and priorities of the G7 countries, and highlight the importance of developing a flexible and diverse energy mix that can meet the needs of different countries and regions.<br>
    </span>  
</div>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.6.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.7.6.1.jpg"></a> <br>

<div class="alert alert-block alert-info">
    <span>
        ${\color{blue}Insights:}$<br>
            1. When it comes to renewable energy sources, each of the G7 countries has its own strengths and areas of focus. <br>
            2. The United States primarily relies on hydropower for its renewable energy mix, with a significant increase in solar energy in recent years. <br><br>
            3. Canada's renewable energy mix is primarily based on hydropower, with a smaller contribution from wind energy. <br>
            4. The United Kingdom and Germany, on the other hand, are mostly reliant on wind energy. France is primarily based on hydropower, but has seen an increase in wind energy as well. <br>
            5. Italy is primarily based on hydropower, but has also seen a significant increase in solar energy. <br><br>
            6. Japan is largely based on hydropower, but has also experienced a significant increase in solar energy in recent years. <br>
            7. These differences reflect the diverse energy needs, resources, and priorities of each of the G7 countries, and highlight the importance of developing a flexible and diverse energy mix that can meet the needs of different countries and regions.<br>
    </span>  
</div>

<a id="Overview"></a>
<h2>   
    <font color = blue>
        <span>
            8. World Energy Overview
        </span>   
    </font>    
</h2>

<a href="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.8.1.jpg"><img align="center" width="auto" height="auto" src="https://github.com/hamid-rahbar/WorldEnergyDataAnalysisPython/blob/main/Plots/P.8.1.jpg"></a> <br>
