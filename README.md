Baltimore Police Redistricting Analysis
================

  - [Overview](#overview)
  - [Data](#data)
  - [Methodology](#method)
  - [License](#license)

## Overview

Redrawn Baltimore Police districts would drastically increase the Western and Eastern districts’ share of the most serious crimes committed in Baltimore while decreasing the Northeastern District’s share. This repository includes the crime data and the code used in the analysis that led to our story: [Proposed Baltimore police districts would lump more violent crime into the most violent districts][www.thebaltimorebanner.com]. But larger, more violent districts could actually be beneficial for Baltimore if police equitably realign resources, experts say.
The Baltimore Police Department's goal was to equally share workload among the city’s nine districts, a term it defines as the number of 911 calls times the number of hours officers spend responding. But this equality would create other inequalities:
- The Western, Eastern and Southwestern neighborhoods will comprise almost half of all city homicides and shootings and the share of the Western and Southwestern neighborhoods will increase.
- If crime trends return to pre-pandemic levels, the Western District will have the highest share of shootings, homicides, aggravated assaults and 911 calls. Redistricting would have increased all four.
- New land and the residents who live there added to the historically violent Eastern and Western districts will lower the per capita rates of homicides and shootings despite more of each occurring in those districts.
- The proposed Northeastern District would have the lowest share of all shootings and homicides if pandemic trends continue with just 7% of each , a drastic drop from 10% and 9%, respectively. Only two other districts would see drops in both categories; their shares are much higher and remained within a percentage point of current levels.
- If pandemic trends are more indicative of the future, the proposed Southwestern district would have by far the most homicides. Nearly one of every five homicides have taken place within the proposed district boundaries since the beginning of 2020.

<a id="data"></a>
## Data

### Pre-pandemic crime trends in current and proposed districts
district | current total | proposed total | current agg assault | proposed agg assault | current homicide | proposed homicide | current shooting | proposed shooting
--- | --- | --- | --- | --- | --- | --- | --- | ---
western | 7.95 | 10.68 | 11.40 | 13.83 | 16.82 | 17.63 | 16.93 | 18.25
southwestern | 10.36 | 9.90 | 12.36 | 12.51 | 14.02 | 16.07 | 14.04 | 15.89
eastern | 8.77 | 10.14 | 11.37 | 12.09 | 14.70 | 14.77 | 14.74 | 13.84
northwestern | 9.88 | 10.07 | 9.75 | 9.20 | 12.83 | 12.09 | 11.02 | 10.36
northern | 11.16 | 10.63 | 8.17 | 9.09 | 6.85 | 9.53 | 6.85 | 9.01
southeastern | 14.23 | 12.92 | 10.98 | 10.22 | 6.85 | 7.91 | 6.60 | 7.86
southern | 11.23 | 11.02 | 12.08 | 11.22 | 9.66 | 7.79 | 11.30 | 9.56
northeastern | 14.80 | 11.45 | 13.46 | 9.45 | 12.34 | 7.73 | 11.40 | 7.55
central | 11.62 | 13.19 | 10.43 | 12.39 | 5.92 | 6.48 | 7.13 | 7.68

### Pandemic crime trends in current and proposed districts
district | current total | proposed total | current agg assault | proposed agg assault | current homicide | proposed homicide | current shooting | proposed shooting
--- | --- | --- | --- | --- | --- | --- | --- | ---
southwestern | 11.23 | 10.25 | 12.51 | 11.77 | 15.55 | 19.08 | 13.91 | 15.47
western | 8.11 | 10.90 | 10.41 | 13.19 | 14.61 | 14.61 | 13.65 | 15.79
eastern | 8.82 | 10.08 | 10.55 | 11.56 | 13.66 | 14.02 | 15.33 | 13.14
northwestern | 10.50 | 10.85 | 10.26 | 10.41 | 13.07 | 12.25 | 10.48 | 9.84
southern | 11.85 | 11.74 | 10.98 | 10.71 | 13.90 | 10.72 | 12.35 | 11.52
southeastern | 13.44 | 12.36 | 10.05 | 10.16 | 7.77 | 7.77 | 8.15 | 9.45
northern | 10.38 | 10.33 | 8.76 | 9.27 | 5.18 | 7.66 | 6.27 | 8.35
central | 11.88 | 13.01 | 11.56 | 12.24 | 5.89 | 7.30 | 9.83 | 9.39
northeastern | 13.79 | 10.47 | 14.93 | 10.69 | 10.37 | 6.60 | 10.03 | 7.06

### 911 calls by districts
district | current_2020_to_current_raw | current pandemic share | proposed_2020_to_current_raw | proposed pandemic share | current_2015_to_2020_raw | current 2015 to 2020 share | proposed_2015_to_2020_raw | proposed 2015 to 2020 share
--- | --- | --- | --- | --- | --- | --- | --- | ---
central | 297419 | 9.58 | 365429 | 11.77 | 262037 | 10.84 | 300309 | 12.42
eastern | 341762.00 | 11.01 | 325825.00 | 10.49 | 256870.00 | 10.63 | 261670.00 | 10.82
northeastern | 331983 | 10.69 | 242664 | 7.81 | 308085 | 12.74 | 215057 | 8.90
northern | 333309 | 10.73 | 366725 | 11.81 | 257046 | 10.63 | 267274 | 11.06
northwestern | 413137 | 13.30 | 388408 | 12.51 | 225674 | 9.34 | 233717 | 9.67
southeastern | 337068 | 10.85 | 321590 | 10.36 | 269178 | 11.13 | 247873 | 10.25
southern | 380547 | 12.25 | 350034 | 11.27 | 261374 | 10.81 | 250244 | 10.35
southwestern | 317145 | 10.21 | 348457 | 11.22 | 291332 | 12.05 | 294302 | 12.17
western | 352991 | 11.37 | 396045 | 12.75 | 285900 | 11.83 | 346869 | 14.35

<a id="method"></a>

## Methodology

### How we analyzed changing BPD districts

Baltimore Police have [redrawn the districts](https://www.baltimorepolice.org/redistricting) using 2020 Decennial Census, workload service data, Part 1 crimes and property crimes data from 2016 to 2021. It defined workload as the number officers who responded to each call times the number of calls.

The Baltimore Banner analyzed the data in light of the pandemic, comparing how the proposed map would impact pre-pandemic rates and those since January 2020. The Banner used Part 1 crime data and 911 call data downloaded from Open Baltimore and combined it with 2020 Decennial Census Data. We are unable to reproduce the workload analysis because we do not have access to data on the number of officers who responded to a call.

We consider pre-pandemic and pandemic crime trends because it is impossible to know which will be more predictive of future crime. Experts do not agree if the pandemic has altered crime trends permanently. Others believe pandemic changes in crime are unlikely to hold, making pre-pandemic trends more representative of future crimes.

The Banner was able to make its own shape files and crosswalks for the proposed districts because they include whole neighborhoods, an existing dataset made available on Open Baltimore and included in Part 1 crime data.

<a id="license"></a>

## License

Copyright 2022, The Venetoulis Institute for Local Journalism

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
