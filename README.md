# capstone_project1_group6
- This project compares the various Environmental, Social and Governance (ESG) factors of USA in the 2010's decade and also against the ESG factors of various other countries.

- Based on the various ESG factors, the performance of the Exchange Traded Funds (ETF) devoted to the ESG, i.e. sustainable investing, in various sectors are compared and their 10 years of returns is projected via Monte Carlo Simulation.

- The end goal is a proposal for the creation of an investment recommendation platform that would cater to people who are focused towards sustainability. The platform will suggest investing in a portfolio, based on the ESG cause that an individual is most concerned about, to drive positive/ sustainable impact on the country.

## Libraries/Technologies used
- os
- csv
- requests
- pandas
- numpy
- panel
- hvplot
- tkinter
- pathlib
- dotenv
- plotly express
- MCforecasttools
- alpaca trade api

## Tools used
- Gitbash
- Github
- Slack
- Jupyter lab
- Panel dashboard
- Microsoft CSV
- Alpaca API
- Google sheets
- Google slides

## Data collected
- ESG indicators on 17 different factors for all the countries, from 1961- 2019 (Source: World Bank)
- Ticker data of ESG focused ETFs in alternative energy, board diversity, education, nuclear power, disease treatment, green building. (Source: ETF Database, Alpaca)

## Notebooks created
- esg_analysis; to compare the ESG progress of USA in the last 10 years and also with 50 other countries.
- esg_returns; to gather the 5-year ticker data of ETFs and project their 10-year return.

## Data exploration and cleanup
  
### * esg_analysis:
- The metadata of all the countries' 17 ESG areas split up into more than 60 different facotors, from 1961- 2019, was pulled in a CSV format from World Bank's website.

- Our period of analysis was narrowed down only to the 2010s decade (10 years) and 9 factors, which we believed are the most important to address. Pandas was used for slicing and cleaning the data

- The following ESG factors were selected.
    - Carbondioxide (CO2) Emission
    - Particulate Matter (PM) exposure
    - Forest area
    - Renewable energy usage
    - Life Expectancy
    - Overweight population
    - Women in legislature
    - Research and Development expenditure
    - GDP growth
    
- Many categories had missing data either for 1 year or multiple years. The missing year was removed from consideration and only the available yearly data was analyzed. For those categories that had only some missing data, it was reset to '0'. 

- Each subset of data was sliced from the metadata, then analyzed and graphs were plotted.

### *esg_returns:
- The 5-year ticker data of the ESG focused ETFs was pulled from Alpaca trade API.

- The following were the sectors of interest
    - Alternative Energy
    - Board diversity
    - Education
    - Nuclear Power
    - Disease treatment
    - Green building
    
- The timeframe of the ticker data is from Dec 1, 2015 to Dec 12, 2019
- The number of simulations for all sectors is 100.
- 10-year return was projected for each of the sectors.
- The investment amount is 10000 USD for all the sectors

- Monte Carlo simulation was run and plotted. Then, the cumulative return distribution was plotted.

- The summary statistics for the Monte Carlo simulation was calculated.

- The lowest and the maximum possible return was calculated, based on 10000 USD initial investment.

## Metrics calculated/ Graphs Plotted
### *esg_analysis:
- For each of the categories, the following was calulated/ plotted.
    - hvplot Bar chart of USA's progress in the last decade.
    - Line plot of USA's progress compared with 2 other random countries
    - Cumulative 10-year mean of all the countries, plotted as a bar.
    
- For a particular category, the top 5 highest or the lowest performing countries for a specified year was calculated.

- In addition, for a particular category, the countries were sorted by the highest or the lowest cumulative mean.

### *esg_returns:
- For each ESG sector, the following was calculated/ plotted.
    - Monte Carlo Simulation and graph
    - Cumulative return distribution plot
    - Summary statistics: 95% lower and upper confidence interval
    - Return on 10000 USD
    
## Dashboard Panel
- Panel visualization functions were defined for each of the plots created in the esg_analysis notebook, to call the plots on the dashboard.

- The plots for each category was arranged by column, using the Panel library.

- Dashboard tabs were created for each category to interactively visualize the plots. 

- Another dashboard was made using the tkinter python library (not covered in class), consisting of the graph interpretation for each of the above ESG category.

## Plot interpretation
- Find on the tkinter dashboard, by running it.

## How to run the panel dashboard?
- Download the file to the local machine and run the following command on the Jupyter Lab terminal to view the interactive plot:
- "panel serve esg_analysis.ipynb --log-level debug --show"

## Conclusion
- Refer to the product_vision readme file.

## Difficulties faced
- The graphs dont display properly on the Panel dashboard. However, the plot is clean individually.
- Lack of complete (free) ESG data of countries from 2010- 2019

## Contributors
- Austin Avent
- Sylvia Li
- Satheesh Narasimman

## People who helped
- Allan Hall, Bootcamp Instructor
- Joel Gonzales, Bootcamp Teaching Assistant
- Khaled Karman, Satheesh's bootcamp tutor

## References
- https://databank.worldbank.org/source/environment-social-and-governance?preview=on#

- https://datacatalog.worldbank.org/dataset/environment-social-and-governance-data

- http://api.worldbank.org/v2/source/75/indicators

- https://www.geeksforgeeks.org/creating-tabbed-widget-with-python-tkinter/

- https://etfdb.com/

- https://etfdb.com/esg-investing/environmental-issues/green-building/

- https://hvplot.holoviz.org/user_guide/Customization.html

- https://hvplot.holoviz.org/user_guide/Plotting.html

- http://holoviews.org/user_guide/Dashboards.html

- https://github.blog/2015-06-08-how-to-undo-almost-anything-with-git/

- https://www.advisorperspectives.com/articles/2020/09/07/the-vanishing-difference-between-esg-and-conventional-funds
    