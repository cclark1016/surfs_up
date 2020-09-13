# surfs_up
## Overview
The purpose of this analysis is to use climate data queried from a database of historical weather station readings to determine if an Ice Cream & Surf shop in Oahu would see revenue significantly affected by rainfall & temperatatures that negatively affect demand for ice cream. 

## Results
- The historic mean temperature in June is 75 degrees while the historic mean temperature in December is 71 degrees

- The standard deviation of average June temperatures is 3.26. This means on 95% of days in June we will expect to have temperatures between 68.5 and 81.5 degrees.

- The standard deviation of average December temperatures is 3.75. This means that in December we will expect to see 95% of days above 63.5 degrees. 

## Summary
The average temperature differences between June and December are about 4 degrees and 95% of days in December will be above 63.5 degrees . If there is not a significant dropoff in ice cream demand somewhere within the 4 degree difference between June and December temperatures it can be expected that Ice Cream sales in December will only be slightly affected by cooler temperature. 

### Additional Queries
Precipitation in month of June:
- precip_query = session.query(Measurement).filter(extract("month",Measurement.date)== 6).all()
- precip_query = [(i.date,i.prcp) for i in results]

Precipitation in month of December:
- precip_query = session.query(Measurement).filter(extract("month",Measurement.date)== 12).all()
- precip_query = [(i.date,i.prcp) for i in results]


