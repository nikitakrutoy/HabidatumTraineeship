# Analysis of houses under Moscow Renovation Program
[Renovation webpage in Russian](https://www.mos.ru/city/projects/renovation/)  
[Some reads in English](https://www.theguardian.com/cities/2017/mar/31/moscow-biggest-urban-demolition-project-khrushchevka-flats)

***Renovation*** - is a resettlement project of people who lived in low-cost apartament buildings, comonly named "Khrushevki", which was developed during the early 1960s
Old buildings will be demolished and the new apartment will rise on their place.

### Data:   
*Dataset1*: 33 thousands buildings with differrent paraments(area, year of construction, etc) and ~4 thousands is in renovation programm  

For more precise analysis of studied type of building ("khrushevki") and area around them 5 districts were selected (3 with a lot of old building, 2 wihtout them)  

*Dataset2*: 5 thousands buildings from chosen districts, subsets of Dataset1  

*Dataset3*: 4kk posts with geotags from vk.com from March 2017 to Augest 2017

## Classification
*2 classes*: in renovation program or not

Classification was done in order to estimate weights vector and find most important features.
3 different classification models have been used: logic regression, decision tree and boosting.
Models was traind with cross-validation on all data.

f1_score values:

|Models/Datasets | 33k  | 5k   |
| -------------  |:----:| ----:|
|Log.regr        | 0.61 | 0.89 |
|DeсisionTree    | 0.71 | 0.91 |
|Boosting        | 0.79 | 0.93 |



## Topic modeling and word2vec 
In oreder to investigate the areas, where people speak about renovation word2vec was traind on data from vk.
Using top50 words similar to "renovation" 2000 post was selected. This words was also used to build a cloud of words.
After that LDA model was trained to compare the result topics with "rennovation" topic.

More info could be found in [notebook](https://github.com/nikitakrutoy/habidatum_traineeship/blob/master/khrushevki/хрущевки2.ipynb)





