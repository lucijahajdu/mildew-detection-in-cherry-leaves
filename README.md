

## Dataset Content
* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/cherry-leaves). We then created a fictitious user story where predictive analytics can be applied in a real project in the workplace.
* The dataset contains +4 thousand images taken from the client's crop fields. The images show healthy cherry leaves and cherry leaves that have powdery mildew, a fungal disease that affects many plant species. The cherry plantation crop is one of the finest products in their portfolio, and the company is concerned about supplying the market with a compromised quality product.



## Business Requirements
The cherry plantation crop from Farmy & Foods is facing a challenge where their cherry plantations have been presenting powdery mildew. Currently, the process is manual verification if a given cherry tree contains powdery mildew. An employee spends around 30 minutes in each tree, taking a few samples of tree leaves and verifying visually if the leaf tree is healthy or has powdery mildew. If there is powdery mildew, the employee applies a specific compound to kill the fungus. The time spent applying this compound is 1 minute.  The company has thousands of cherry trees, located on multiple farms across the country. As a result, this manual process is not scalable due to the time spent in the manual process inspection.

To save time in this process, the IT team suggested an ML system that detects instantly, using a leaf tree image, if it is healthy or has powdery mildew. A similar manual process is in place for other crops for detecting pests, and if this initiative is successful, there is a realistic chance to replicate this project for all other crops. The dataset is a collection of cherry leaf images provided by Farmy & Foods, taken from their crops.


* 1 - The client is interested in conducting a study to visually differentiate a healthy cherry leaf from one with powdery mildew.
* 2 - The client is interested in predicting if a cherry leaf is healthy or contains powdery mildew.


## Hypothesis and how to validate?
* Infected leaves are visually detected due to their powdery white layer on the surface of leaf.

* Hypothesis is validated by collectin an image dataset from the client and creating an image montage for healthy and infected leaves.
* Hypothesis is tested by average image analysis

## The rationale to map the business requirements to the Data Visualisations and ML tasks
### Business Requirement 1
* Study should include analysis on:
  * average images and variability images for each class (healthy or powdery mildew)
  * the differences between average healthy and average powdery mildew cherry leaves
  * an image montage for each class
### Business Requirement 2
* ML system needs to preredict wheather a cherry leaf is healthy or contains powdery mildew.
* Dashboard should show features of showing an image montage and a prediction feature


## ML Business Case
In this section, we will look at individual elements of the case and justify how it is an ML business case.

1. What are the business requirements?<br>
   The client would like a tool to identify healthy cherry leaves from powdery mildew contained.
   We understand that ML can be used to identify images and differentiate one from the other if a model has been trained to an acceptable accuracy level.

2. Is there any business requirement that can be answered with conventional data analysis?<br>
   The Requirement 1 can be solved using traditional data analysis methods. However, the second requirement can not be solved using traditional data analysis approaches therefore we would need an ML tool to tackle the challenge.

3. Does the client need a dashboard or an API endpoint?<br>
   The client needs a dashboard.

4. Can you break down the project into Epics and User Stories?<br>
   The project can be broken down into epics and stories. 

5. Ethical or Privacy concerns?<br>
   The client provided the data under an NDA (non-disclosure agreement), therefore the data should only be shared with professionals that are officially involved in the project. 

6. What does the client consider a successful project outcome?<br>
   The client can visually see and differentiate healthy leaves from powdery mildew-contained ones.
   An image montage can be created that shows both types of leaves

The client will also be able to predict if a leaf is healthy or contains powdery mildew by uploading images to the dashboard.

7. What are the model's inputs and intended outputs?<br>
   The input is a cherry leaf image and the output is a prediction of whether the cherry leaf is healthy or contains powdery mildew.

8. Does the data suggest a particular model?<br>
   The data suggest it is a binary classification model.

9. What are the criteria for the performance goal of the predictions?<br>
   An accuracy of 97% has been agreed with the client; however, the model has been trained to a 99% accuracy.

10. How will the client benefit?<br>
    The client will not supply the market with a compromised product. Furthermore, the client will also be able to scale up their operations in detecting mildew on other farms by minimising manual work.

## Dashboard Design
* A project summary page, showing the project dataset summary and the client's requirements.
* A page listing your findings related to a study to visually differentiate a cherry leaf that is healthy from one that contains powdery mildew
* A page containing:
* A link to download a set of cherry leaf images for live prediction (Kaggle repository).
* A User Interface with a file uploader widget. The user should have the capacity to upload multiple images. For each image, it will display the image and a prediction statement, indicating if a cherry leaf is healthy or contains powdery mildew and the probability associated with this statement.
* A table with the image name and prediction results, and a download button to download the table.
* A page indicating your project hypothesis and how you validated it across the project.
* A technical page displaying your model performance.


## Unfixed Bugs
* 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file. 


## Main Data Analysis and Machine Learning Libraries
The following main libraries were used in the project
- **numpy** It is a foundation for pandas and matploblib, both libraries have been built on it. It is used to convert the images into an array for analysis and ML training, calculating means and sd. 
- **pandas** It is used to manipulate the dataset. For example, we used pandas dataframe to save an image prediction report.
- **matplotlib** It is used to plot images such as augmented images and data images.
- **seaborn** It is used to plot image datasets, especially with multiple axes and more features. For example, we used it to plot image montages.
- **tensorflow** ML framework that is used to build, train, and validate the model
- **streamlit** It is used to build the dashboard
- **keras** It is used for image analysis such as augmentation and ML model training.



## Credits 

- The code for data modelling, visualisation and ML model creation, training, and deployment has been taken from Code Institute lessons and walkthrough projects.
- The dashboard and readme.md file has been built using the provided templates
- The code for building pages and help with read me file was taken from [KhanRana](https://github.com/KhanRana/PP5-mildew-detection-in-cherry-leaves/).



## Acknowledgements (optional)
* I would like to thank to my mentor for the support and help.
