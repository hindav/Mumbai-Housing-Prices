# Mumbai Housing Prices 2025 – With Coordinates 🏙️📍
**Real Mumbai Real Estate Dataset (Geospatial Enabled)**

![Mumbai](https://img.shields.io/badge/City-Mumbai-blue) ![Rows ~20K](https://img.shields.io/badge/Rows-~20,000-green) ![Coords](https://img.shields.io/badge/Geospatial-Lat/Long-orange)

Real and up-to-date residential property listings from Mumbai & suburbs (scraped 2023–2025), structured similar to the famous California Housing dataset — but this time for the Maximum City!

Perfect for:
- Price prediction (regression)
- Geospatial analysis & mapping
- Comparing Mumbai vs California housing markets
- Beginner-to-advanced ML projects

### File
`mumbai_housing_2025.csv` (~20k rows)

### Columns (10 total)

| Column              | Description                                      | Example                  |
|---------------------|--------------------------------------------------|--------------------------|
| longitude           | Longitude of the property                        | 72.94808                 |
| latitude            | Latitude of the property                         | 19.08957                 |
| housing_median_age  | Median age of buildings in the area (years)      | 33                       |
| total_rooms         | Total rooms in the property                      | 1438                     |
| total_bedrooms      | Total bedrooms                                   | 770                      |
| population          | Population in the micro-area                     | 3061                     |
| households          | Number of households                             | 1133                     |
| median_income       | Median income of households (in tens of thousands ₹) | 0.416899 → ~4.17 Lakh/year |
| median_house_value  | Price in ₹ (target variable)                     | 1641025 → ₹1.64 Crore    |
| ocean_proximity     | Proximity category (adapted for Mumbai)          | NEAR OCEAN, INLAND, NEAR BAY, etc. |

**Note**: `ocean_proximity` categories have been meaningfully mapped to Mumbai geography:
- `NEAR OCEAN` → Sea-facing or coastal (Bandra, Worli, Marine Drive, etc.)
- `NEAR BAY` → Near creeks/backwaters
- `<1H OCEAN` → Within 1 km of sea/creek
- `INLAND` → Suburbs far from water

### Quick Start (Python)
```python
import pandas as pd
df = pd.read_csv('mumbai_housing_2025.csv')
df.head()
