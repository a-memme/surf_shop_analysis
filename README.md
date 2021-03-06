# Surf Shop Analysis
## Purpose
Parsing weather data for the months of June and December in Oahu using SQLAlchemy in order to provide insight on weather appropriateness/business sustainability for a potential surf & ice cream shop on the island.

## Results 
Results from the analysis revealed that:
- Average temperature through both months are in a desirable range (i.e 74.9°F in June, and 71°F in December).
- Max temperatures through both months are also in a desirable range (85°F in June, 83°F in December). 
- Minimum temperatures through both months are slightly undesirable, but manageable depending on frequency (64°F in June, 56°F in December). 

*(Reference both tables below - top table is in reference to June temperatures, bottom to December)*.

<img width="206" alt="june_weather" src="https://user-images.githubusercontent.com/79600550/116790958-24d14980-aa85-11eb-85a7-c81291a842e3.png">

<img width="196" alt="dec_weather" src="https://user-images.githubusercontent.com/79600550/116790961-269b0d00-aa85-11eb-9165-920e7a730d1c.png">

## Summary 
The above analysis gives a basic interpretation and generalization of some summary statistics regarding temperature in Oahu through the months of June and December across a number of years. Here, we can make predictions based on average, minimum and maximum temperatures to estimate what the overall temperature will be year round, thus providing valuable data to base business decisions on. 

However, other analyses and/or queries can be performed to get at further areas of interest in the data. In the additional_analysis folder, additional analysis was performed, achieving the following:
- Parsing for date and preciptation using SQLAlchemy ORM, paralelling the June/December temperature query originally performed. Precipitation values for the months of June and December were isolated, and respective summary statistics were gathered (See SurfsUp_Challenge_Additional_Code file in additional_analysis folder).
- Calculating the mode precipitation for June and December, as well as mode temperature for June and December. SQLAlchemy ORM was used in this instance to query only single preciptation values and single temperature values with the June and December filters intact (no corresponding date data displayed). 
- Using Numpy's unravel function to format temperature data to be appropriately plotted in a box-and-whisker plot (reference Fig1_Oahu_temps.png in additional_analysis folder)

With this additional analysis, valuable data was revealed. In the original analysis, an extremely vital measurement of central tendency was left out - mode. The importance of mode in this instance is quite straightforward - the most frequently occuring instance of temperature or precipitation will help form a better picture of weather appropriateness for a surf/ice cream business, i.e understanding how many days of the year weather would typically positivley, or negatively impact business. Here, results revealed desirable mode values of 76°F and 71°F for the months of June and December respectively. With this, there is strong indication of an evenly distributed data set as mode and mean for both months are very close or identical in value. Mode values for precipitation were also desirable, both providing a value of 0 for the months of June and December.

The summary statistics for precipitation were within the ranges of desirability as well - i.e data displaying enough rain to provide luciousness to the island, but not enough to impede on surfing and/or ice-cream eating conditions. June and December summary statistics are represented in the figures below, repsectively:

<img width="174" alt="june_precip" src="https://user-images.githubusercontent.com/79600550/116794202-450b0380-aa99-11eb-999c-0451d0f7239f.png">

<img width="181" alt="dec_precip" src="https://user-images.githubusercontent.com/79600550/116794204-463c3080-aa99-11eb-8d1d-ff9cffbb74e9.png">

Finally a box-and-whisker plot was created to visually display temperatures for June and December (See below or reference the additional_analysis folder/Fig01_Oahu_temp.png) . The box-and-whisker specifically is of importance in this analysis as it allows one to visualize where outliers are situated, and gather a greater, more in-depth understanding of the data at hand. For instance, we know that the minimum temperature for December is 56°F, however, given the box-and-whisker visualization, one can see that this value is outside 1.5x IQR and is considered an outlier in reference to other values. A more accurate minimum temperature to consider for the month of December would be 63°F where the range ends. Similarily, the same could be observed of max temperature values. When considering both months, one could estimate strong temperature occurrences within the 63°F-83°F range, and therefore, be more confident in Oahu's weather conditions year-round in relation to the business of interest.

<img width="731" alt="oahu_temp" src="https://user-images.githubusercontent.com/79600550/116794328-3ec95700-aa9a-11eb-8403-ff242ddb1d16.png">
