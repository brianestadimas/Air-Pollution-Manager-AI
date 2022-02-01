# AI Air Pollution Manager
Final project for the Building AI course

## Summary
In order to reduce Air Emissions and improve Air Quality in an area, Air Pollution Manager **AI will take part as fault detectors on Buildings that are harmful to the Air Environment.** <br/>
This AI Program measures Air Pollution Rate and Air Quality Index (AQI) on buildings. Program will collect input from Carbon Footprint rate (CO, CO2, CFCs, etc), particulate matter (PM), weather, and any other pollutant data in a building. Compares to other buildings around in that area. Then decisively detects fault on them. <br/>

## Background
Air pollution has been a worldwide problem, which makes it important to know the possible consequences of uncontrolled pollution. According to WHO, Air pollution kills an estimated seven million people worldwide every year and it affect major threat to humanity health and climate changes. The combined effects of ambient (outdoor) and household air pollution cause millions of premature deaths every year, largely as a result of increased mortality from stroke, heart disease, chronic obstructive pulmonary disease, lung cancer and acute respiratory infections. This also affect [global warming](https://www.eea.europa.eu/publications/2599XXX/page009.html), [life expectancy](https://journals.lww.com/epidem/Fulltext/2013/01000/Effect_of_Air_Pollution_Control_on_Life_Expectancy.4.aspx), [wildlife problem](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7044178/), and depletion of ozone layer.

![image](https://user-images.githubusercontent.com/28497662/151737966-2dd77292-4eca-4f8a-a90f-fd74407fe517.png) 

Jakarta has above [160 AQI by 2022](https://www.iqair.com/indonesia/jakarta), which is three times higher than WHO recommendation. When observing the data collected in Jakarta over the last few years, it becomes apparent that the levels of air quality have actually gotten worse instead of better. <br/>

Detective and preventive measures are required to prevent further impact and [loss](https://earth.stanford.edu/news/how-much-does-air-pollution-cost-us#gs.o5rkoq). **Technology in this field required as detective approach. With the help of Artificial Intelligence, it can increase efficiency, accuracy, and reduce operational cost.**

## How is it used?
Possible implementation for Air Pollution Manager AI : <br/>
- Goverment, in order to detect improper companies in an area. This will help goverment for auditing and take action.
- Smart City App, as personal usage (household) and community awareness.
- Property (Estate), as helper to implement green area concept and increase air quality.
- Educational and Research

## Data sources and AI methods
### Data Sources
For early stage of training, datasets will be collected through : <br/>
- Universal open dataset for regional air quality index.<br/>
https://www.kaggle.com/open-aq/openaq <br/>
https://www.kaggle.com/kerneler/starter-aqi-jakarta-hanoi-bangkok-86904a66-c/data
- Goverment Dataset (climatology agency) in specific targeted area.
- **Sample with minimum of 150 buildings** (100 households, 30 stores, and 20 factories) for every expanded region.

Supporting data : <br/>
- Weather data for past month along with AQI (include pH, temperature, winds)
- Carbon footprint dataset
- Pollutant sources dataset


### Machine Learning Methods
**Supervised learning** will be used with [Artificial Neural Network (ANN)](https://en.wikipedia.org/wiki/Artificial_neural_network) method. The implementation will be using **Tensorflow**, **Keras**, and data processing library such as Pandas and Numpy. <br/>
![image](https://user-images.githubusercontent.com/28497662/151931756-43f3c284-67f1-4224-9d2f-d5457263e949.png) <br/>
Early iteration stage : <br/>
1.  Collect primary and supporting dataset
2.  Data preprocessing, includes data cleaning, normalization, and reshaping.
3.  Split Train and Test data using 10-fold cross validation, therefore we will have 70% training dataset, 20% test dataset, and 10% cross validation.
4.  Build [logistic regression](https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc) function
5.  Build activation function (hidden layer), dropout layer, and output layer.
6.  Compile and fit the model.
7.  Train the model until desired epoch.
8.  At this stage, we will have finished model in form of Keras Model (.h5)
9.  Evaluate the model and repeat steps to receive desired accuracy.
10.  Testing

Continous stage : <br/>
- Sample dataset that have been collected will be added to Input dataset and going through the process of Training. Therefore every expanded region, the dataset will increase and transferred into Training process. This implies on every buildings that have been predicted, the AI will collect the input data to dataset.
- Input variables can also increase. Example currently we have PM25, O2, O3, Carbons, weather, etc. as input, then in the future, we can detect Air Pollution  Rate based on spectrum color of skies (with enough dataset). Indeed, it will be included into dataset.

## What next?
**Detect Air Pollution Rate base on spectrum color of sky using mobile phone camera.** <br/>
![image](https://user-images.githubusercontent.com/28497662/151937793-ff73ade8-619a-4a15-bada-a8788f6717a7.png) <br/>
This isn't hard to implement later on as [I have similar App here](https://github.com/brianestadimas/safemask-ai). However I will be focusing on MVP of current product first. The concept is using Convolutional Neural Network (CNN) with [Tensorflow 2 Object Detection API Framework](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/).

## Challenges
**1. Data Collection and Authority**<br/>
This is the biggest challenge for this AI Program as we will collect sample data directly from buildings (households and factories). It requires authority from goverment or collaboration with Smarty City App, without these I would say it is against ethics. Another way is to find voluntary or rewarding system.<br/>

**2. Limitation of Resources (as well as Knowledge in this Field)**
Currently I am the only developer for AI Pollution Manager AI. To determine weights and validity, person or institution within knowledge in this field is required to collaborate in this project. <br/>
<br/>
If you are from goverment, institutional, or related field and wish to collaborate, kindly [reach me out here](https://www.linkedin.com/in/brianestadimas/).






