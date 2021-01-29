# How Coronavirus impacts population distribution? Monthly Population Prediction Based on Machine Learning and Satellite Imagery: Evidence from Italy, 2020

### !!! This is the ongoing program of mine which is being updated from time to time. 

<strong>The key codes will be demonstrated shortly after the completion of the dissertation and the possible publication.</strong>

Author: <a href="https://www.researchgate.net/profile/Keer_Zhang3">Keer Zhang</a>, Peking University, Beijing, P. R. China

Instructor: Tao Liu, Peking University, Beijing, P. R. China

Abstract： Deep leaning is penetrating into the urbanization spatial prediction; however, it merely calculates the variables for Cellular Automata (CA) and limited by the CA frameworks. In this study, I construct an entirely deep learning model based on land classification and night-time light remote sensing data to predict where for further urbanization. This model adopts the Convolutional Neural Networks (CNN), specifically ResNet, to achieve more layers and accurate results. In contrast to extant research, this methods require simple and open data and provide a novel deep-learning framework, which will provide researchers and planners with new methodological references in predicting urbanization development, and perhaps other application (e.g., traffic flow and population migration prediction).

<em>keywords</em>: Machine learning, Convolutional Neural Networks (CNN), ResNet, Urbanization Prediction, Remote Sensing Data

This study will be proceeded with the following order:

### Study Area: 84Cities in Italy

<ul>
    <li>Beijing-Tianjin-Hebei</li>
    <li>Yangtze River Delta</li>
    <li>Pearl River Delta</li>
</ul>

<img src="https://www.globaltimes.cn/Portals/0/attachment/2011/2216b8ba-70bd-4660-a2d2-affba4e55a43.jpeg" width="50%" style="margin: 0 auto;">

### Dataset:

<ul>
    <li><em>Urban Atlas Dataset (2012)</em>: Population (2012), road length (2012) (from <a href='https://land.copernicus.eu/local/urban-atlas/urban-atlas-2012'>EEA Corpernicus Program</a>)</li>
    <li><em>Land Cover Classification (1992-present)</em>: land cover (2012, 2019) (from <a href='https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-land-cover?tab=overview'>EEA Corpernicus Program</a>)</li>
    <li><em>DEM Data (2016)</em>: DEM  (from <a href='https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-land-cover?tab=overview'>EEA Corpernicus Program</a>)</li> 
    <li><em>Night-time Light (2012-present)</em>: Monthly night-time light (2012, 2013, 2020) (from <a href="https://eogdata.mines.edu/download_dnb_composites.html">VIIRS Day/Night Band Nighttime Lights Dataset</a>)</li>
</ul>



### Step 1: day-time satellite imagery -> land cover classification (Model I)

The major reference is a brilliant essay of Zhang et al. (<a href="https://linkinghub.elsevier.com/retrieve/pii/S0034425718305236">2019</a>) . During my CNN training, my land cover classification is referred mainly from <a href='https://cds.climate.copernicus.eu/cdsapp#!/dataset/satellite-land-cover?tab=overview'>EEA</a> dataset. 

<br><img src="https://datastore.copernicus-climate.eu/c3s/published-forms/c3sprod/satellite-land-cover/overview.png" width="50%" style="margin: 0 auto;">


### Step 2: land cover classification -> future urbanization prediction (<a href="https://github.com/past-urbanist/CNN-Model-for-Urbanization-Prediction/blob/master/resnet.ipynb">Model II</a>)

In this step, land cover data (resolution: 300m * 300m) of the 3 past years (e.g., 2000, 2005, and 2010) is the input layer, and the urban-nonurban data of the predicted year (e.g., 2015) is the label layer. ResNet model is employed in this process to achieve a deeper network and a better result. This part is partly open above in the Jupyter Notebook right now on my GitHub. The *pynb* file is run in the Google Colab GPU. 

I have some problem of overfitting right now and I plan to fix it by expanding my datasets and dataloaders. 

### Step 3: introduction of night-time satellite imagery to improve Model II (Improved Model II)

After adjusting the resolution of night-time satellite imagery, I will append the data of corresponding years as input layers of Model II, which (at least I hope) will improve the prediction effects greatly. 
