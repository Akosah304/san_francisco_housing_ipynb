# san_francisco_housing_ipynb
## Background

Proptech, the application of technology to real-estate markets, is an innovative domain in the fintech industry. As an analyst at a proptech company that wants to offer an instant, one-click service for people to buy properties and then rent them. The company wants to have a trial of this offering in the San Francisco real-estate market. If the service proves popular, they can then expand to other markets.

My approach is to use my data visualization skills, including aggregation, interactive visualizations, and geospatial analysis, to find properties in the San Francisco market that are viable investment opportunities.

## Problem

This challenge we create a Jupyter notebook that contains analysis of the housing rental market data for San Francisco. The analysis will be complete with professionally styled and formatted interactive visualizations.

## Technology
The following python modules are used in the application. Remember to install these packages via Terminal for MacOS/Linux or GitBash for windows clients.

pandas - pandas is used to interact with data packages, plot data frames, create new dataframes, describe abailable data, and helps traders and fintech proffesionals organize financial data to perform advanced decisionmaking.

pathlib - Allows the user to specify the path to a data frame / any data in a csv file.

hvplot.pandas

If hvplot and pandas are both installed, then we can use the pandas.options.plotting.backend to control the output of pd.DataFrame.plot and pd.Series.plot. This notebook is meant to recreate the pandas visualization docs.

## Approach
This assignment requires to create a visualization by using hvPlot and GeoViews. The main task in this Challenge is to visualize and analyze the real-estate data in the Jupyter notebook. The approach is fivefold:

Calculate and plot the housing units per year.

Calculate and plot the average prices per square foot.

Compare the average prices by neighborhood.

Build an interactive neighborhood map.

Compose your data story.

## Calculate and plot the housing units per year.
For this part of the assignment, we'll use numerical and visual aggregation to calculate the number of housing units per year, and then visualize the results as a bar chart. This will done in the following three steps:

Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.
Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.
Style and format the line plot to ensure a professionally styled visualization.

## Calculate and Plot the Average Sale Prices per Square Foot
For this part of the assignment, we'll use numerical and visual aggregation to calculate the average prices per square foot, and then visualize the results as a bar chart. To do so, we'll complete the following steps:

Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?
Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.
Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.
Style and format the line plot to ensure a professionally styled visualization.

## Compare the Average Sale Prices by Neighborhood
For this part of the assignment, we'll use interactive visualizations and widgets to explore the average sale price per square foot by neighborhood. To do so, we'll complete the following steps:

Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.
Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.
Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.
Style and format the line plot to ensure a professionally styled visualization.

## Build an Interactive Neighborhood Map
For this part of the assignment, we'll explore the geospatial relationships in the data by using interactive visualizations with hvPlot and GeoViews. To build our map, we'll use the sfo_data_df DataFrame (created during the initial import), which includes the neighborhood location data with the average prices. To do all this, we'll complete the following steps:

Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.
Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.
Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame. Note that the first cell uses the Pandas concat functionLinks to an external site. to create a DataFrame named all_neighborhoods_df. The second cell cleans the data and sets the “Neighborhood” column. Be sure to run these cells to create the all_neighborhoods_df DataFrame, which we’ll need to create the geospatial visualization.
Using hvPlot with GeoViews enabled, we'll create a points plot for the all_neighborhoods_df DataFrame. The following parameters will be defined:
geo parameter to True
size parameter to “sale_price_sqr_foot”.
hover_cols parameter to the index column "Neighborhood"
size_max parameter to “25”.
zoom parameter to “11”.
color parameter to “gross_rent”.
frame_width parameter to 700.
frame_height parameter to 500.
descriptive title.

## Compose Your Data Story
We'll conclude by answering the following questions:

How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighborhoods across San Francisco?
What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you would suggest for investment, and why?