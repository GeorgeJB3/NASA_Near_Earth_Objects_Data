# NASA_Near_Earth_Objects_Data

## Points of clarification I would seek from the stories provided.

### User story 1
- Orbital period, what precision is required ie days, hours, mins


### User Story 2
- Clarify the time period instead of assuming it is the same as User Story 1

### Both User Stories
- What unit of measurement is required for object size ie. kilometers, miles, meters, feet
- Is the minimum and maximum size needed or the average size
- For 'Individual object profiles', what data should be shown
- Should filtering be based on size, distance, hazard classification
- The API only allows 7 days of data per request. is this enough for the task or do we need to batch request over the 50 year period

## Improvements

I currently have 2 tables ```near_earth_objects``` and ```close_approaches_with_earth```.
An improvement I would like to make is to create a star schema and implement data normalisation to remove redundant and duplicate data.
 - Example:
   - Fact table with columns object_id, approach_id.
   - Dimension tables: dim_size with columns such as object_id, min_size, max_size, average_size. dim_approach with columns approach_id, date, time, miss_distance,       velocity.
  
NOTE: API_KEY left in repo as it's a free key so no security risks
