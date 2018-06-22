# Data Acquisition

This section describes and imports data on weather in Silicon Valley.  The analysis presented in subsequent sections shows that the range of temperatures in Silicon Valley has widened in 2015 as compared to the previous 10-year period (from 2005 to 2014).

Data cleaning and processing are described in the [next section](https://eagronin.github.io/sv-weather-prepare/).
 
The data was downloaded from the Coursera website.  The original source of the data is The National Centers for Environmental Information (NCEI) [Daily Global Historical Climatology Network](https://www1.ncdc.noaa.gov/pub/data/ghcn/daily/readme.txt) (GHCN-Daily).  The GHCN-Daily is comprised of daily climate records from thousands of land surface stations across the globe.  Each row in the datafile corresponds to a single observation on daily record temperature as reported by weather stations located in Silicon Valley, in the vicinity of Sunnyvale, CA.

The following features are available:

```
    id : station identification code
    date : date in YYYY-MM-DD format (e.g. 2012-01-24 = January 24, 2012)
    element : indicator of element type
        - TMAX : Maximum temperature (tenths of degrees C)
        - TMIN : Minimum temperature (tenths of degrees C)
    value : data value for element (tenths of degrees C)
```

The following code imports the data:

```python
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
from matplotlib.dates import DateFormatter
import pylab

def read_weather_data():
    
    df = pd.read_csv('/Users/eagronin/Documents/Data Science/Portfolio/Project Data/weather data.csv')
    
    return df
```

Next step: [Data Preparation](https://eagronin.github.io/sv-weather-prepare/)
