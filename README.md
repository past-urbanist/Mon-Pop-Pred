# How Coronavirus impacts population distribution? Monthly Population Prediction Based on Machine Learning and Satellite Imagery: Evidence from Europe, 2020

### !!! This is the ongoing program of mine which is being updated from time to time. 

<strong>The key codes will be demonstrated shortly after the completion of the dissertation and the possible publication.</strong>

Author: <a href="https://www.researchgate.net/profile/Keer_Zhang3">Keer Zhang</a>, Peking University, Beijing, P. R. China

Instructor: Tao Liu, Peking University, Beijing, P. R. China

<em>keywords</em>: Machine learning, Coronavirus, Population prediction, Night-time light data

## Dataset:

<ul>
    <li><em>Urban Atlas Dataset (2012)</em>: Population (2012), road length (2012) (from <a href='https://land.copernicus.eu/local/urban-atlas/urban-atlas-2012'>EEA Corpernicus Program</a>)</li>
    <li><em>Land Cover Classification (1992-present)</em>: land cover (2012, 2019) (from <a href='https://land.copernicus.eu/pan-european/corine-land-cover'>EEA Corpernicus Program</a>)</li> 
    <li><em>Night-time Light (2012-present)</em>: Monthly night-time light (2012, 2013, 2020) (from <a href="https://eogdata.mines.edu/download_dnb_composites.html">VIIRS Day/Night Band Nighttime Lights Dataset</a>)</li>
</ul>

## Study Area: 22 Cities in Europe

Urban Atlas Dataset (2012) has covered almost every city throughout Europ. 

<img src="https://github.com/past-urbanist/Mon-Pop-Pred/blob/main/img/Study Area.png" alt="Study Area" width="50%" style="margin-left:25%">

<div style="text-align:center">Figure 1. Study Area (<i>Source</i>: Authors)</div>

## Step 1: Data Preparation

This study has adopted the gridded measurement  (30 arc sec), which is consistent with the resolution of the usual population datasets (e.g., LandScan, WordPop).

The major essence is to predict population through night-time light. To achieve it, the controlled variables are proposed as city id, land cover, road length, distance to city centre, and so on. All of the controlled variables and the dependent variable (population density) are obtained directly or indirectly from EEA Copernicus Program, after resampled into grids. Most of these variables can be regarded constant (city id, DEM, etc.) or changed little (road length, distance to city centre).

<br><img src="https://github.com/past-urbanist/Mon-Pop-Pred/blob/main/img/Data.png" alt="Data Sample" width="50%">

<div style="text-align:center">Figure 2. Data Sample (A case in in Roma) (<i>Source</i>: Authors)</div>

## Step 2: Machine Learning in Regression

First, RF indentifies and sceens the unpopulated areas for a clear structure of population, which achieves the >90% precision and >90% recall.
Then, DL is used to train and predict the remaining 3/4 data with R<sup>2</sup> = 0.76.

## Step 3: Population Distribution Analysis

After adopting the optimal Machine Learning model to predict the monthly gridded population data in 2020, aided by monthly night-time light data in 2020. The next step is analysis, which will be updated in April (I hope so). Multiple indexes will be extracted from 84 cities and corelated with the pandemic data as well.

## Reference
<ul>
    <li>Briggs, D. J., Gulliver, J., Fecht, D., & Vienneau, D. M. (2007). Dasymetric modelling of small-area population distribution using land cover and light emissions data. Remote Sensing of Environment, 108(4), 451–466. https://doi.org/10.1016/j.rse.2006.11.020</li> 
    <li>...</li>
</ul>
    
