# Geospatial Analysis and Outlier Detection in Election Data

This project focuses on ensuring the integrity and transparency of electoral processes through geospatial analysis and outlier detection in election data. By analyzing polling data from the Yobe region, I identified polling units with voting patterns significantly different from their geographical neighbors, which might indicate anomalies or potential fraud.

## Objectives
The primary objective of this analysis is to identify polling units that exhibit different voting patterns from their geographical neighbors. Such outliers could indicate potential irregularities, warranting further investigation. By leveraging advanced geospatial techniques, I aim to provide a comprehensive overview of the voting landscape, highlighting areas that deviate from expected patterns.

## Methodology
### Data Collection and Cleaning

Election data including polling units, geographical coordinates, and vote counts for different parties (APC, LP, PDP, NNPP) was obtained online and pre-processed to remove inaccuracies. The geographic coordinates (longitude and latitude) of each polling unit was also obtained using Awesome Table Geocoder.

## Geospatial Neighbor Analysis

KD-Tree algorithm was used to find neighboring polling units within a 1-kilometer radius for each unit.
This step helps in comparing voting patterns across proximate units efficiently.

### Outlier Detection

For each polling unit, the average number of votes received by each party among its neighbors was calculated and the outlier scores computed by comparing the averages with the actual votes received.
A higher outlier score indicates a significant deviation from neighboring units.

### Results

The analysis revealed several polling units with outlier scores indicating notable deviations from their neighbors. These outliers were systematically identified and ranked for each political party, providing a clear and detailed list of polling units that may require further scrutiny. Box plots and maps were also used to illustrate the outliers in each party.

### Conclusion

This project provides a robust framework for identifying potential irregularities in election data using geospatial analysis and outlier detection. The insights derived can inform further investigations and support efforts to ensure election integrity and transparency.

### Dependencies
pandas
numpy
scipy
folium
openpyxl
