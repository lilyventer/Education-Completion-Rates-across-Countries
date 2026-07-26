# Python Project: Education Completion Rates Across Countries


## Import environments

``` python
import pandas as pd
import statsmodels.api as sm
```

## In Terminal

pip3 install openpyxl This allows the excel file to be read.

## Bringing in the Data

``` python
file_path = '~/Library/Mobile Documents/com~apple~CloudDocs/MSBAAcademics/Python/PotentialDataSets/CompletionRateData.xlsx'
```

``` python
pd.read_excel(file_path, sheet_name='Primary')

pd.read_excel(file_path, sheet_name='Lower secondary')

pd.read_excel(file_path, sheet_name='Upper secondary')
```

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }
&#10;    .dataframe tbody tr th {
        vertical-align: top;
    }
&#10;    .dataframe thead th {
        text-align: right;
    }
</style>

|  | ISO3 | Country_US | Region_US | Sub-region_US | Development Regions_US | Total_US | Gender_Female_US | Gender_Male_US | Residence_Rural_US | Residence_Urban_US | ... | WealthQuintile_Fourth_US | WealthQuintile_Richest_US | Data source_US | Time period_US | Population data | Unnamed: 18 | Unnamed: 19 | Unnamed: 20 | Unnamed: 21 | Unnamed: 22 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0 | AFG | Afghanistan | SA | SA | Least Developed | 22.89534 | 14.36536 | 32.315559 | 16.607441 | 38.913071 | ... | 23.041981 | 46.00013 | DHS 2015 | 2015.0 | 2838749.0 | 1380667.0 | 1458082.0 | 2.115013e+06 | 7.237360e+05 | 0.254949 |
| 1 | ALB | Albania | ECA | EECA | More Developed | 77.94796 | 79.857063 | 76.226807 | 69.100288 | 83.281387 | ... | 86.269928 | 94.473183 | DHS 2017-18 | 2018.0 | 115351.0 | 53510.0 | 61841.0 | 4.577256e+04 | 6.957844e+04 | 0.603189 |
| 2 | DZA | Algeria | MENA | MENA | Less Developed | 46.431679 | 59.164452 | 34.630589 | 35.473091 | 52.63472 | ... | 54.440559 | 71.954803 | MICS 2019 | 2020.0 | 1792844.0 | 878622.0 | 914222.0 | 4.907199e+05 | 1.302124e+06 | 0.726290 |
| 3 | AND | Andorra | ECA | WE | More Developed | NaN | NaN | NaN | NaN | NaN | ... | NaN | NaN | NaN | NaN | 1378.0 | 665.0 | 713.0 | 1.645119e+02 | 1.213488e+03 | 0.880615 |
| 4 | AGO | Angola | SSA | ESA | Least Developed | 18.7439 | 15.21019 | 23.698139 | 3.587311 | 24.791439 | ... | 20.194349 | 50.236111 | DHS 2015-16 | 2016.0 | 2304438.0 | 1160585.0 | 1143853.0 | 7.946991e+05 | 1.509739e+06 | 0.655144 |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |
| 232 | NaN | Sub-Saharan Africa | SSA | NaN | NaN | 27.139825 | 24.517603 | 30.580722 | 14.515915 | 44.190132 | ... | 31.612346 | 54.768732 | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN |
| 233 | NaN | Eastern & Southern Africa | NaN | ESA | NaN | 24.483467 | 23.465614 | 25.78399 | 13.669898 | 40.909224 | ... | 25.495936 | 50.885104 | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN |
| 234 | NaN | West & Central Africa | NaN | WCA | NaN | 29.415109 | 25.42541 | 34.655156 | 15.401085 | 46.273332 | ... | 36.836565 | 58.08586 | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN |
| 235 | NaN | Least developed countries | NaN | NaN | LDC | 21.653922 | 19.356057 | 24.375379 | NaN | NaN | ... | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN |
| 236 | NaN | World | NaN | NaN | NaN | 44.695655 | 43.601486 | 46.085723 | 30.985658 | 59.579358 | ... | 48.137189 | 69.395016 | NaN | NaN | NaN | NaN | NaN | NaN | NaN | NaN |

<p>237 rows × 23 columns</p>
</div>
