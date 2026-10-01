Plan: Does unemployment increase during recessions?
1. Question
Does unemployment increase during recessions?

Expectation: Yes, I think that unemployment will increase during recessions because during economic downturns, there is reduced hiring and increased layoffs.

2. Data Sources
My data will come from the FRED API.

Unemployment Rate
Series ID: UNRATE
Source: Bureau of Labor Statistics through FRED
Recession Indicator
Series ID: USREC
Source: National Bureau of Economic Research through FRED
Python tools:

fredapi (to pull data from the FRED API)
python-dotenv (to load my API key)
pandas
matplotlib
statsmodels
API key: My FRED API key will be stored in a .env file and loaded in the notebook with python-dotenv. The .env file will be listed in .gitignore so the key is never in the repo.

3. Cleaning Steps
Pull monthly data from FRED.
Restrict data to 2000-present.
Merge unemployment and recession datasets.
Handle missing values by dropping months where either series is missing.
Create variables showing whether the economy was in recession.
Create a variable for the monthly change in the unemployment rate.
Calculate average unemployment during recessions and expansions.
4. Charts
Line chart of unemployment rate over time, with recession periods shaded.
Bar chart comparing average unemployment during recessions vs non-recessions.
All charts will have a title, axis labels with units, and the data source.

5. Statistical Test
Run two simple regressions:

Unemployment Rate = β0 + β1(Recession Indicator)
Change in Unemployment Rate = β0 + β1(Recession Indicator)
The second regression tests whether unemployment actually rises faster during recessions.

6. What would support or contradict my expectation
Supporting evidence:

A positive β1 would show unemployment is higher, and rises faster, during recessions.
Contradicting evidence:

A zero or negative β1 would suggest recessions are not associated with higher unemployment.
7. Limitations
-This only shows correlation, not direct causation.
-Monthly data may miss some economic changes due to shutdowns, etc.
-Other factors also influence unemployment, not just the economic state of the U.S.