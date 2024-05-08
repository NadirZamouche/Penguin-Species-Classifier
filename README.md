
![18-species-of-penguins](https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/e3505b07-679a-4e53-b823-d312fe79b136)

## 📝 Description
🐧 Penguin Species Profiler Project: Delved into the fascinating world of penguin species differentiation through an intensive analysis of their physical traits. Leveraging machine learning techniques, I explored five distinct models to classify penguins into their respective species. After rigorous evaluation, I implemented Support Vector Machine (SVM) as the optimal model, fine-tuning its parameters to achieve superior accuracy.

📊 Additionally, I visualized feature contributions, shedding light on the critical factors influencing species classification. Through meticulous examination, I unearthed the unique characteristics defining each species, providing valuable insights into penguin morphology and diversity.

## ⏳ Dataset
The 'penguins.csv'  file contains data on various attributes. Here's a breakdown of each column:
- Culmen Length: The length of the culmen, which is the upper ridge of a bird's beak, measured in millimeters (mm). It is an important morphological characteristic used in bird identification and classification.
- Culmen Depth: The depth of the culmen, measured from the top of the ridge to the bottom of the beak, typically in millimeters (mm). Culmen depth can vary between species and is another important feature for distinguishing between different types of birds.
- Flipper Length: The length of the flipper, which is the wing of a penguin, measured in millimeters (mm). Flipper length is crucial for penguins as it directly relates to their ability to swim and navigate underwater.
- Body Mass: The mass or weight of the penguin's body, usually measured in grams (g) or kilograms (kg) in this case in grams. Body mass is essential for understanding the health, growth, and reproductive success of penguins, as well as their overall fitness and survival in their habitats.
- Species: The species of the penguin, categorized based on various characteristics including morphology, behavior, and habitat preferences. Understanding the different species of penguins helps researchers and conservationists better manage and protect these unique birds and their environments. In this case we only have 3 from ranked 0 to 2.

## :mag: Data Cleansing
* Filled missing values using species-specific mean.
* Created boxplots for each column to check for outliers. Here is a box plot for Population column:



* Ploted histograms for each column to see if the data is balanced or not:



* Ploted heat map for correlation matrix:



* Applied the min max scaler since there were no outliers within the data.

## :desktop_computer:	Modeling
* Utilizing the cleansed data. I partitioned the data into two sets: 75% designated for training and 25% allocated for testing using StratifiedShuffleSplit to ensure representative stratification across the dataset.
* Employed five distinct classification models, systematically assessing for overfitting through cross-validation techniques. Subsequently, I computed various evaluation metrics for each model and discerned the optimal choice based on the overall metrics scores.

<img width="473" alt="Evaluation Metrics" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/b0a51247-230a-4854-b6dd-ad67f3d6fdd6">

* Conducted hyper-parameter tuning for eXtream Gradient Bossting Regressor, meticulously exploring various settings to ascertain the most effective combination for optimal performance.

<img width="262" alt="Best Parameters Combination" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/bb93ef3d-9468-4a54-b284-2368f58f5512">

* Tested the final model on the test set and got relatively better results:

<img width="162" alt="Evaluation Metrics (Tuned Model)" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/479970f1-28d1-4e94-8443-9d838507afc5">

* Retested the final model on the whole entry dataset and got even better results:

<img width="134" alt="Evaluation Metrics (Whole Set)" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/f96d4cf8-9219-4af4-8b81-2fe07b42dc13">

## :chart_with_upwards_trend: Feature Importance
* Here is a chart showing the sorted contribution of each column to the target column "median_house_value":

<img width="459" alt="Feature Importance" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/588f84d1-4657-499e-8f8a-64ea290257ef">

## 🔨 Conclusion
The analysis highlights the importance of ocean proximity, particularly being inland, followed by island properties, in predicting house prices. Additionally, median income is also a significant factor in determining housing prices, although slightly less influential compared to ocean proximity. This information can be valuable for understanding the drivers of housing market dynamics and making informed decisions in real estate investments or policy-making.
