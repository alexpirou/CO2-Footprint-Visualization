# Population & CO2 Footprint Visualizer 1970-2010

![Map Visualization](/PopMap.png "CO2/Populations Map Visualization and Slider")
![Bar Chart Visualization](/PopChart.png "Populations Bar Chart")
![Map Visualization Hover Effect](/MapHover.png "CO2/Populations Map Visualization Hover Effect")

## Contributors

Alexander Pirouznia, Carl Chen, Jason Lee

## Description

The primary data sources we used were the [World Population](https://www.kaggle.com/datasets/iamsouravbanerjee/world-population-dataset) and [CO2 Emissions datasets](https://www.kaggle.com/datasets/ulrikthygepedersen/co2-emissions-by-country), which both include data for all countries, allowing us to correlate emissions and population figures across multiple years (1970-2010). To create the map outlines, we utilized the [World Map GeoJSON](https://gist.github.com/markmarkoh/2969317). For the contour maps, we used a dataset from [Google Developer Docs](https://developers.google.com/public-data/docs/canonical/countries_csv), which provided country coordinates for generating the contours. The World Population dataset was then used to create the bar chart, with country-specific values that enabled us to link the countries on the map with corresponding color fills for easy comparison.

This visualization is designed to help users explore the relationship between population levels and CO2 emissions for the years where our datasets overlap. Initially, we planned to include a line chart for a selected country alongside a CO2 contour map. However, we later revised this concept to feature a bar chart displaying the top countries, with matching color highlights on the map. Users can also hover over any country to see its corresponding population and CO2 emission values. The contours offer a general view of CO2 emissions, while the bar chart serves as a quick reference for the populations of the top 5 countries. Users can hover over specific countries for a closer look, allowing them to quickly grasp the overall trends. As users adjust the year slider, both the population and emission data update in real time, reflected in the map and bar chart visualizations.

## Design Rationale

Our visualization employs several interactive elements, dependent on several variables. For one was linking the bar chart (of population size) to the contour map of CO2 emissions. To show the correlation between the two, we used a common variable named specificYear which represents time (or year). Because we are using data from our dataset from the years 1970 to 2010 (these were the years all datasets had in common), with a step of 10 (intervals of 10 years), it was important that we showed the evolution of population size and CO2 emissions throughout the years and how they changed. Not only does this track the ever evolving dataset, it also accounts for the correlation between the bar chart and the contour map. Each year, users can see where the contours are the most vibrant and deepest, that correspond with CO2 emission values as seen in the legend. Furthermore users can toggle and hover over individual countries. By hovering over a unique country, the name and CO2 emissions value of that year is presented in a tooltip. 

On the split hand, the bar chart changes each year to show the top five most populated countries and their respective population sizes, including how they increase or decrease throughout the years. Each of the five most populated countries are presented in a different color for clear differentiation. Finally, came the challenge of how to represent the timeline feature (from 1970-2010). Two ideas immediately sprung to mind. For one, there was a drop down menu with all the years in our time range. By clicking the drop down menu and selecting a specific country, the visualization would be interactive with both the contour map and bar chart changing to reflect the selected year. This allows for clear distinction of the different years, however relies on more interactions from the user in making multiple clicks to achieve their desired outcome. The other option was to use a slider, similar to what we did in a past homework assignment. Parallel to the drop down menu, both the contour map and bar chart would change to reflect the respective year. While the slider allows for minimal user interaction, as clicks are limited, there is less distinction in year selection, as getting to a certain year isn’t immediately recognizable and easy to discern. Users may have to play around with the slider for longer than expected to reach their intended year, which in turn would limit user-friendliness. Because of this, the challenge presented multiple solutions each with their own pros and cons. After building out both solutions, we decided on the slider with the included feature of showing the year when toggled with. Because there are only five selections (1970, 1980, 1990, 2000, 2010), we didn’t believe there would be too much room for ambiguity when attempting to select a time frame. The slider allowed for a seamless change between 10 year periods and was well represented visually with the contour map and the bar chart and their respective data. 


## The Story

Our visualization project began from a curiosity about the relationship between global population growth and CO2 emissions over time. By examining data from 1970 to 2020, we aimed to uncover how shifts in population might correlate with CO2 emissions across various countries, ultimately revealing an intriguing relationship between population growth, industrialization, and environmental impact. While we initially expected somewhat of a straightforward link between high population and high emissions, the visualization suggests that population size alone does not fully determine a country’s CO2 output. Other factors, such as industrialization, energy consumption patterns, and economic growth, appear to play more influential roles in CO2 levels than we initially thought.

For example, economically advanced countries with relatively small populations—like the United States and certain Western European nations—have disproportionately high CO2 emissions, particularly in earlier decades when fossil fuels presumably fueled their industrial growth. In contrast, emerging economies like China and India display significant emissions spikes from the 2000s onward, which might be linked to rapid industrialization. Additionally, some densely populated countries maintain relatively low emissions, suggesting that variations in energy sources and economic practices could impact environmental outcomes in distinct ways.

In conclusion, this project provides a nuanced perspective on the complex and multifaceted relationship between population and CO2 emissions. Rather than showing a simple correlation, the visualization suggests that a range of factors—including economic and industrial development—may influence a country’s environmental footprint over time. The insights offered by this visualization underscore the importance of examining multiple dimensions when analyzing global emissions, as the interactions between population, economy, and environmental impact are far from one-dimensional.