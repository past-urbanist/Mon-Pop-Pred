# How Coronavirus impacts population distribution? Monthly Population Prediction Based on Machine Learning and Satellite Imagery: Evidence from Italy, 2020

### !!! This is the ongoing program of mine which is being updated from time to time. 

<strong>The key codes will be demonstrated shortly after the completion of the dissertation and the possible publication.</strong>

Author: <a href="https://www.researchgate.net/profile/Keer_Zhang3">Keer Zhang</a>, Peking University, Beijing, P. R. China

Instructor: Tao Liu, Peking University, Beijing, P. R. China

<em>keywords</em>: Machine learning, Coronavirus, Population prediction, Night-time light data

## Dataset:

<ul>
    <li><em>Urban Atlas Dataset (2012)</em>: Population (2012), road length (2012) (from <a href='https://land.copernicus.eu/local/urban-atlas/urban-atlas-2012'>EEA Corpernicus Program</a>)</li>
    <li><em>Land Cover Classification (1992-present)</em>: land cover (2012, 2019) (from <a href='https://land.copernicus.eu/pan-european/corine-land-cover'>EEA Corpernicus Program</a>)</li>
    <li><em>DEM Data (2016)</em>: DEM  (from <a href='https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-land-cover?tab=overview'>EEA Corpernicus Program</a>)</li> 
    <li><em>Night-time Light (2012-present)</em>: Monthly night-time light (2012, 2013, 2020) (from <a href="https://eogdata.mines.edu/download_dnb_composites.html">VIIRS Day/Night Band Nighttime Lights Dataset</a>)</li>
</ul>

## Study Area: 84 Cities in Italy

Urban Atlas Dataset (2012) has covered almost every city throughout Europe with 84 cities in Italy. Considering Italy has initiatively and significantly influenced by the pandemic since January, 2020, I have taken Italy as a case for monthly population prediction. 

<img src="https://github.com/past-urbanist/Mon-Pop-Pred/blob/main/img/Study Area.png" alt="Study Area" width="50%" style="margin-left:25%">

<div style="text-align:center">Figure 1. Study Area (<i>Source</i>: Authors)</div>

## Step 1: Data Preparation

This study has adopted the gridded measurement  (0.04 &deg; × 0.04 &deg;), which is consistent with the resolution of night-time light dataset.

The major essence is to predict population through night-time light. To achieve it, the controlled variables are proposed as city id, land cover, road length, distance to city centre, and DEM. All of the controlled variables and the dependent variable (population density) are obtained directly or indirectly from EEA Copernicus Program, after resampled into grids. Most of these variables can be regarded constant (city id, DEM, etc.) or changed little (road length, distance to city centre).

<br><img src="https://github.com/past-urbanist/Mon-Pop-Pred/blob/main/img/Data.png" alt="Data Sample" width="50%" style="margin-left:25%">

<div style="text-align:center">Figure 2. Data Sample (A case in in Roma) (<i>Source</i>: Authors)</div>

## Step 2: Machine Learning in Regression

I am currently trying different models (Decision Trees, Random Forest, SVM, and Deep Learning) for the optimal outcomes.

In short, for now, Random Forest proves the best (R<sup>2</sup> = 0.808). Since I am still trying more possibilities, it can be updated any time. 

## Step 3: Population Distribution Analysis

After adopting the optimal Machine Learning model to predict the monthly gridded population data in 2020, aided by monthly night-time light data in 2020. The next step is analysis, which will be updated in April (I hope so). Multiple indexes will be extracted from 84 cities and corelated with the pandemic data as well.

## Reference
<ul>
    <li>Briggs, D. J., Gulliver, J., Fecht, D., & Vienneau, D. M. (2007). Dasymetric modelling of small-area population distribution using land cover and light emissions data. Remote Sensing of Environment, 108(4), 451–466. https://doi.org/10.1016/j.rse.2006.11.020</li> 
    <li>...</li>
</ul>
    
