
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
* Created boxplots for each column to check for outliers. Here is a box plot for CulmenLength column:

<img width="542" alt="Box Plot for Culmenlength" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/35d14888-b365-404e-87f2-9f4b454869ef">


* Ploted histograms for each column to see if the data is balanced or not:

<img width="752" alt="Histograms" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/f023efcf-a381-4487-80c9-dd8736d555e0">


* Ploted heat map for correlation matrix:

<img width="537" alt="Correlation Matrix" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/e69d2456-2155-44d3-9f55-eb457b67793b">


* Applied the min max scaler since there were no outliers within the data.

## :desktop_computer:	Modeling
* Utilizing the cleansed data. I partitioned the data into two sets: 75% designated for training and 25% allocated for testing using StratifiedShuffleSplit to ensure representative stratification across the dataset.
* Employed five distinct classification models, systematically assessing for overfitting through cross-validation techniques. Subsequently, I computed various evaluation metrics with the multi_class set to ovr "OneVersusRest" for each model and discerned the optimal choice based on the overall metrics scores.

<img width="451" alt="Evaluation Metrics" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/4b0fc406-258f-4a89-b929-d4c4b4921a14">


* Conducted hyper-parameter tuning for Support Vector Classifier, meticulously exploring various settings to ascertain the most effective combination for optimal performance.

<img width="242" alt="Best Parameters Combination" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/6c1563ca-8729-4455-b7d0-03d8350c7ecb">

* Tested the final model on the test set and got relatively better results:

<img width="146" alt="Evaluation Metric (Tuned Model)" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/1186fc72-7af0-488c-9815-0afca32e62e3">

* Retested the final model on the whole entry dataset and got even better results:

<img width="106" alt="Evaluation Metric (While Set)" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/1a57a099-731b-42f8-9bd9-ebcd6cf41ca2">

## :chart_with_upwards_trend: Feature Importance
* Here is a chart showing the sorted contribution of each column to the target column "species":

<img width="497" alt="Feature Importance" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/4f26d707-06ad-4be4-9c9b-ca0bebeddba8">

## 🔨 Conclusion
The analysis indicates the distinguishing characteristics for each penguin species as follows:
- Species 0: CulmenLength (32.1 - 46) mm ; CulmenDepth (15.5 - 21.5) mm ; FlipperLength (172 - 210) mm ; BodyMass (2850 - 4775) g.
- Species 1: CulmenLength (40.9 - 59.6) mm ; CulmenDepth (13.1 - 17.3) mm ; FlipperLength (203 - 231) mm ; BodyMass (3950 - 6300) g.
- Species 2: CulmenLength (40.9 - 58) mm ; CulmenDepth (16.4 - 20.8) mm ; FlipperLength (178 - 212) mm ; BodyMass (2700 - 4800) g.

As shown earlier, Culmen Length serves as the primary factor in determining the species to which a penguin belongs.
Also, this model has shown very excellent results where he has correctly classified 270 penguins out of 271, meaning he only missed 1 therfore it can be implemented for later use as you can see in this illustration:

<img width="523" alt="Results" src="https://github.com/NadirZamouche/Penguin-Species-Classifier/assets/95188070/2d9f97a1-241c-4f11-ac87-a97d27bd9ffd">

