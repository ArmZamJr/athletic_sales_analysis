# athletic_sales_analysis

## External resources
https://pandas.pydata.org/docs/reference/api/pandas.core.groupby.SeriesGroupBy.nlargest.html#pandas.core.groupby.SeriesGroupBy.nlargest
    top_5_df = group_df.nlargest(5, 'Total_Products_Sold')
    top_5_df = group_df.nlargest(5, 'Total_Products_Sold')

01-Lesson_Plans > 04-Data-Preparation-1 > 3 > Activities > 05-Ever_Data_Cleaning > Solved > spring_cleaning.ipynb
csv_data.isnull().sum()

resampling_melting_DataFrames_solution.ipynb
 converted_ufo_df['datetime']= pd.to_datetime(converted_ufo_df['datetime'], errors='coerce')
 combine_df['invoice_date']= pd.to_datetime(combine_df['invoice_date'], errors='coerce')

## chatgpt.com & AskBCS Learning Assistant
 # Show the total number of women's athletic footwear sold for each retailer, region, state, and city.
womans_footwear_sold_df = wom_ath_foo_df.groupby(['retailer','region','state','city'])\
    ['units_sold'].agg(Womens_Footwear_Units_Sold=("sum"))
# Rename the "units_sold" column to "Womens_Footwear_Units_Sold"
womans_footwear_sold_df.rename(columns={'units_sold':'Womens_Footwear_Units_Sold'}, inplace=True)
#womans_footwear_sold_df["Womens_Footwear_Units_Sold"].value_count().head(5)
#wfus_counts = womans_footwear_sold_df["Womens_Footwear_Units_Sold"].value_counts()
#top5_wfus_df = wfus_counts.head(5).index.tolist()
top_5_womens_footwear_units_sold = womans_footwear_sold_df.sort_values(by='Womens_Footwear_Units_Sold', ascending=False).head(5)
top_5_womens_footwear_units_sold
# Show the top 5 results.
#op5_womans_footwear_sold_df = womans_footwear_sold_df.nlargest(5, 'Womens_Footwear_Units_Sold')
#top5_wom_ath_foo_df

 
