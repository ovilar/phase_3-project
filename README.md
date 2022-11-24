# ML Project - Tanzanian Water Pump Status

## Overview

Using the from <a href='https://taarifa.org/'>Taarifa and</a> the <a href='https://www.maji.go.tz/'>Tanzanian Ministry of Water</a>, I create several models to predict which water pumps are functional or not. To simplify the process, I will only work with two prediction labels: functional and not functional, and will apply all the underlying processes from a Machine Learning (ML) workflow standpoint. 

## Business Problem

Impoverished countries have difficulties in having access to clean water. Water poverty is responsible for a series of illnesses. Anecdotal evidence from the <a href='https://www.tanzaniawaterproject.org/how-were-making-a-difference/water-as-a-word-health-issue/'>Tanzanian Water Project</a> lists that:
<ul>
    <li>1/6 of the world population lack access to safe water;</li>
    <li>88% of the diseases are caused by unsafe water drinking;</li>
    <li>The average American uses 100-175 gallon of water daily, whereas the average African uses 5 gallon of water daily;</li>
    <li>Water poverty negatively impacts education, local economies, agriculture and gender equality.</li>
</ul>
Furthermore, it is estimated that people living in water poverty struck places usually have to walk around 3-5 miles per day to have access to questionable water supply. 

The stakeholders are the Tanzanian public policy makers and government, NGO's and the general public - not only the ones that use that well, but all the other communities and people interested.
<div style="width=1026px; height=986px;">
    <img src="https://github.com/ovilar/phase_3-project/blob/main/img/img01.png" alt="Water Pump Geo Location by Status - Tanzania" width="70%" height="70%">
</div>

## Data and Analysis

The data can be found at <a href='https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/25/'>DrivenData</a>. Some basic Exploratory Data Analysis (EDA) and cleaning is performing on this dataset, as well joining its several sources. Most of the variables are categorical (i.e. dummies) and the final dataset has more than 55,000 rows.


## Machine Learning Workflow
I use three different models to assess their predictive abilities in spotting whether a well is functional or not. The usual workflow starts with building pipelines so I can apply imputers and encoders to the DataFrame. After those steps, I run the models and when applicable, tune their hyperparameters using Grid Search and Cross Validation. 

Furthermore, whenever assessing which model is the best, we should have in mind which loss function or metric we are going to use to evaluate its performance. Since the presence of both false positives and false negatives can be costly to our stakeholders, I posit that the best sought-out metric should be the f1-score. This metric will balance the combination of precision and recall, helping stakeholders. The performance of the models can be found below:

<div style="width=1243px; height=976px;">
    <img src="https://github.com/ovilar/phase_3-project/blob/main/img/img02.png" alt ="ML models' scores on testing data" width="60%" height="60%">
</div>
## Conclusion
The logistic regression model provides a 80% adhesion to predict whether a water pump - given its features - is functional or not. This is helpful to aid in the design of public policies, when/which water pumps need to be fixed and providing informational assets to communities that use water pumps. 

### Further Research
Even though the data has its limitations, it is a rich dataset to work with. Further research could indicate not also functional and not functional, but also consider the original label of functional needs repairs. Furthermore, combining the dataset with socio-economical Tanzania statistics can provide more assertiveness when designing public policies.

## Instructions

This repository provides basic guidelines on how to navigate through this notebook and its material. For the sake of space, I do not make the dataset available.

Here you will find:

<ul>
    <li><a href="https://github.com/ovilar/phase_3-project/blob/main/presentation.pdf">Presentation file;</a></li>
    <li>Jupyter Notebook;</li>
    <li>README.md file;</li>
    <li>A .gitignore from GitHub;</li>
    <li>Image Folder.</li>
</ul>

Feel free to reach out if you have any critique, suggestion or correction.