# GeoSpatial Data Project

The main purpose of this project is to locate a company from the gaming industry covering as many requirements as possible.

## Requirements covered 

    - Near successful tech startups that have raised at least $1M (same city)
    - A child care center not more than 500 metres far from the office
    - An airport not more than 5km far from the office
    - A Starbucks not more than 5km far from the office
    - A vegan restaurant not more than 500 metres far from the office
    - A basketball stadium not more than 10km far from the office

## Proceedings

Firtly, on the "Filtering DataFrame" notebook I connected with the "companies" Mongo Database and I obtained only the companies that followed the first requirement. My filter was companies founded after 2010 (startups) and companies that have raised at least $1M from investors. Once I had my dataframe filtered, I built some functions to obtain the coordinates of the different companies. Once I had that I built a map to show the different areas we were going to look at in the next step. 

After filtering our dataframe, on the "API" notebook, I loaded the filtered dataframe and started making calls to the FourSquare API. I coded different functions to check if every single location in the filtered dataframe met the requirements the client asked for. After having this information, I added different columns in the dataframe to build a scoreboard of the requirements covered by every location. 

Finally, since I had two different locations with the same score I coded a little bit more complex function that also returned the exact distance to the closest Starbucks. With this last comparison I could finally decide an exact location. 
