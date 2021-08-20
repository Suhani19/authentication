
# Predicting-Billboard-Hits-Using-Spotify-Data-DS3-200721

The Billboard Hot 100 Chart1 remains one of the definitive ways to measure the success of a popular song. We investigated using machine learning techniques to predict which songs will become Billboard Hot 100 Hits.





## 

![App Screenshot](https://upload.wikimedia.org/wikipedia/commons/2/2b/Billboard_Hot_100_logo.jpg)


## TECHNOCOLAB INTERNSHIP PROJECT:


1)Dataset for songs were collected from Bilboard.com and Millions Songs Dataset. Songs were from year 1990-2018

2)Extracted Songs were labeled either 0 or 1 .Here 0 means billboard not hit,and 1 means billboard hit .

3)Audio Features for each song were extracted from the Spotify web API and the final dataset was provided to our team.

4)Task was to take input from user about audio features and to predict whether the Song will be in the billboard list or not

5)After cleaning the data, a dataset of approx. 10000 songs was created.

# Exploratory Data Analysis -

Dropped the duplicates present in the dataset and then plotted graphs:-

                1) The countplot of songs to hit billboard or not:
![distribution of top100](https://user-images.githubusercontent.com/66556476/130225045-8549dbbb-2954-47da-b57c-c6407af235f0.png)

                2) Distribution of Genre
![distribution of genre](https://user-images.githubusercontent.com/66556476/130225259-43293e64-0f0f-4bf0-b7c9-27719eef8d4c.png)
                
                3)Distribution of song features 
![129669862-7695364f-93f3-40b9-bfa0-3199f7d8b415](https://user-images.githubusercontent.com/66556476/130225897-0d521ff5-115a-4ac7-9ce8-4c055bd5f78d.png)

                4)Distribution of frequency over three decades
![frequency vs decade](https://user-images.githubusercontent.com/66556476/130225957-faa3e75e-7f38-42ab-9cb7-9a72da272135.png)

                5)Correlation between columns 
![correlation](https://user-images.githubusercontent.com/66556476/130227153-4b1ab457-fb7e-4f79-8411-148a9a6eeda1.png)

                6)Feature v/s Decade 1990-2000

![129670022-bd55bd60-e4e3-4a70-bf01-de4951532228](https://user-images.githubusercontent.com/66556476/130225850-fe95029f-e14a-4eda-b18b-28e2d528a164.png)

                7)Feature v/s Decade 2000-2010
![129670772-7eb20227-4dd7-47a0-818e-c31883f664a7](https://user-images.githubusercontent.com/66556476/130225857-3be05f34-eb5e-406a-a11e-81e448cb3b8d.png)

                8)Feature v/s Decade 2000-2010
![129670928-44ccd9ec-9c48-4559-b3c9-d5b4995dcc97](https://user-images.githubusercontent.com/66556476/130225939-9ac0ce3d-ee84-45de-8882-62026e8ffc99.png)

                
                9)Feature Comparisons
![energy vs loudness](https://user-images.githubusercontent.com/66556476/130225978-3b23e702-85ec-41d3-88fe-95fffaa5f726.png)

The graphs in the code show the separability in the data when compared across two unique Spotify features; this suggests that data may separate across an n-dimensional feature space. Given this, the problem can alternatively be posed as an unsupervised learning problem where clustering methods can classify the data.

         
## STEPS INVOLVED IN BUILDING MODELLING:
-> Dropped the unnecessary columns
-> Balanced the output classes
-> Scaled the data with min max scaler
-> Splitted the datasets into train and test data(80/20)
-> Passed our preprocessed data into our logistic regression modela and Linear Discrimanant Analysis(LDA) and trained the data
-> We also performed hyperparameter tuning

## Observations: (Logistic Regression)
1)ACCURACY:67

2)ROC:0.66

3)PRECISION: (70 FOR 0 AND, 65 FOR 1)

4)RECALL: (58 FOR 0 AND , 76 FOR 1)

## Observations (LDA):
ACCURACY:68

2)ROC:0.67

3)PRECISION: (69 FOR 0 AND, 66 FOR 1)

4)RECALL: (60 FOR 0 AND , 75 FOR 1)

## Screenshot of 

![roc1](https://user-images.githubusercontent.com/66556476/130228799-b5a0a9a5-d647-41de-a48e-0f6bf0947e69.png)

![cl1](https://user-images.githubusercontent.com/66556476/130228820-3f8edef4-2d88-4930-af7e-05abfc8228d7.png)

![roc2](https://user-images.githubusercontent.com/66556476/130228862-1471176b-080f-4368-b512-f6b074522bc3.png)

![cl2](https://user-images.githubusercontent.com/66556476/130228880-514e4db0-990b-4474-a358-e39e1eb1ac10.png)






  

## Tools/libraries used for deployment:
1) FLASK: Flask is a web application framework written in Python. It has multiple modules that make it easier for a web developer to write applications without having to worry about the details like protocol management, thread management, etc.

2) HEROKU: Heroku is a container-based cloud Platform as a Service (PaaS). Developers use Heroku to deploy, manage, and scale modern apps. Our platform is elegant, flexible, and easy to use, offering developers the simplest path to getting their apps to market.

3)HTML,css
## Deployment Steps :
1)First we need to create a folder which will contain all the files required for deployment
2)We need to have static folder, which will contain images
3)templates= will have html and css codes
4)app.py which will have a code that will predict the outcomes by taking datas and render with html files
5)model.pkl file should be there (saved model)
6)requirements.txt will contain the neceessary libraries which we used to build a model
7)Procfile is used to run application on heroku cloud platform


## Deployment of Project

To deploy this project run

```bash
    To run locally - python app.py
     To run this project run in browser - https://billboardhot100-predictionapp.herokuapp.com/
```
## Deployment Screenshots -
![1](https://user-images.githubusercontent.com/66556476/130234893-be8eb86e-07e5-4a06-86ca-c30f7ad97bb7.png)

![2](https://user-images.githubusercontent.com/66556476/130234898-d7392378-eb33-450d-b004-77193855098b.png)

![3](https://user-images.githubusercontent.com/66556476/130234902-7f426569-1b16-4ca9-a395-8c0d77ed2ea7.png)

![4](https://user-images.githubusercontent.com/66556476/130234908-07b3fe46-0592-4e8d-bca4-f7d58e4319a2.png)

![5](https://user-images.githubusercontent.com/66556476/130234918-3f135943-903f-4e21-8d11-ab294140787a.png)

![6](https://user-images.githubusercontent.com/66556476/130234924-1da68ea2-0774-4fb7-8c2c-1b97d36502f6.png)

![7](https://user-images.githubusercontent.com/66556476/130235001-cec98887-8f2b-4c2f-8cc9-a521184f8a8b.png)

![8](https://user-images.githubusercontent.com/66556476/130235009-d15108f5-e71f-420c-8203-f8692513469f.png)


  
## Authors

Suhani

- [Github](https://github.com/Suhani19/)

- [Gmail](https://suhanichhabra19@gmail.com) 


Tanya

- [Github](https://github.com/tanyarayat)
- [Gmail](https://tanyarayat@gmail.com)


  