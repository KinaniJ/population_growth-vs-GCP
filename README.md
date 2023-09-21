# population_growth-vs-GCP
This data set I from the public dataset in google console. 
The data was from two tables: Sustainable Development Goals (UN SDG) Indicators (UN Statistics Division) and World Development Indicators (WDI).
I used the below sql query to join data   

SELECT UN_SDG.geoareaname, UN_SDG.timeperiod, UN_SDG.value as
GDP_per_Capita_growth, WB_WDI.country_name, WB_WDI.year, WB_WDI.value as WB_Population FROM `bigquery-public-data.un_sdg.indicators` as UN_SDG JOIN `bigquery-public-data.world_bank_wdi.indicators_data` as WB_WDI on WB_WDI.country_name = UN_SDG.geoareaname WHERE UN_SDG.seriesdescription like '%Annual growth rate of real GDP %' AND UN_SDG.timeperiod = '2016' AND WB_WDI.indicator_name = 'Population, total' AND WB_WDI.year = 2016
I then saved the data and uploaded to Google data Studio for vizualization. 
Here us the report link https://lookerstudio.google.com/s/hXu-Z6kHea4

  


