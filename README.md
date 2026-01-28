# THE INFLUENCE OF VITORIA EDDY IN THE ABUNDANCE OF SEABOB SHRIMP *Xiphopenaeus* spp. (HELLER) IN THE BRAZILIAN EAST COAST
Leandro Bonesi Rabelo, Júlio Neves de Araújo, Agnaldo Silva Martins
## Overview
This repository contains the data and RMarkdown code for the manuscript: **"The influence of Vitória Eddy in the abundance of seabob shrimp *Xiphopenaeus* spp. (Heller) in the Brazilian east coast"**. 

The study investigates how mesoscale oceanographic processes, specifically primary productivity and bottom temperature, drive the abundance of seabob shrimp near the Caravelas Estuary (Abrolhos Bank). We utilized a 19-year time series (2001–2020) of Catch Per Unit Effort (CPUE) data, originated from the Environmental Monitoring Program of the Caravelas Maritime Terminal, to build Generalized Additive Models (GAMs) that account for both environmental variability and historical changes in sampling effort.

## Data Acquisition

### Environmental Data
* **Primary productivity**: Derived from Global Ocean Colour Copernicus Satellite Observations (OCEANCOLOUR_GLO_BGC_L4_MY_009_104; available at https://doi.org/10.48670/moi-00281).
* **Bottom potential temperature**: Obtained from the Global Ocean Physics Analysis and Forecast (GLOBAL_MULTIYEAR_PHY_001_030; available at https://doi.org/10.48670/moi-00021), provided by the Copernicus Marine Service.
* **River flow**: Available via the Hidroweb portal from the National Water Agency (ANA, 2023; available at: https://www.snirh.gov.br/hidroweb/apresentacao).

### Biological Data (*Xiphopenaeus* spp.)
The raw data (`data_Rabelo_et_al.xlsx`) consist of three spreadsheets collected between September 2001 and March 2020:
* **Factors**: Monthly averages of the environmental data acquired as described above.
* **CPUE**: Abundance and effort data for each individual sampling trawl.
* **Coordinates**: Longitude and latitude in UTM for each sampling trawl location.

**Key Variables in the Dataset:**
* `tw_g`: Total weight of the sample expressed in grams (g).
* `effort_min`: Sampling effort duration expressed in minutes (min).
* **CPUE Calculation**: The relative abundance (Catch Per Unit Effort) was derived from these variables and expressed as $kg \cdot h^{-1}$.

**Sampling Methodology:**
* **Method**: Bottom trawl nets (9 m wide) operated at an average speed of 2 knots near the Caravelas estuary.
* **Sampling Grid**: The monitoring grid underwent seven spatial alterations over the 19-year period. The effect of these variations in sampling effort was formally incorporated into the final model building.
* **Time-series Gaps**: 
    * Monitoring interruptions: Jan/02, Jul–Aug/03, Jul/05–Jan/07, Apr–Dec/07, and Jan–Apr/16.
    * Closed season (*defeso*): Periodic gaps in April and October (2008–2019).
