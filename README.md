# World Energy Data Analysis (1900-2020)
### Python Jupiter Notebook

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
Please refer to the Python Code.
    
<a id="Importing"></a>
<h2>   
    <font color = blue>
        <span>
            3. Reading and Understanding the Data:
        </span>   
    </font>    
</h2>
Please refer to the Python Code. <br><br>
    
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
- Here is the link to the dataset source: <a href='https://github.com/owid/energy-data'> Click Here </a> <br>
    

