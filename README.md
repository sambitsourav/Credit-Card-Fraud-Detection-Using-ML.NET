# Credit-Card-Fraud-Detection-Using-ML.NET
**Approach**
Step 1-The data fetched from devices have a fixed schema so we can define our input and output schema accordingly. In this case, we have used a Credit Card Fraud Detection Dataset which is already PCA transformed and can be found [here](https://www.kaggle.com/mlg-ulb/creditcardfraud). The aim is to binary classify data between fraudulent and benign.

Step 2- Create a class to hold the input schema with the column names as the properties of the class. Do the same for output schema something like this:![image.png](/.attachments/image-5bcb31be-ada1-4687-8acd-33c94f57564e.png)

Step 3- Create a WebApp and import the Microsft.ML libraries and create Get requests( to fetch the results) and Post requests(to post the data against which we need prediction).In this project, we have used LbfgsLogisticRegression, Average Perceptron, and Auto Ml model.

Step 4- The Auto Ml is a special library in C# which automatically searches for all algorithms for the problem statement and chooses the best algorithm to train the model.Here is a sample of Auto Ml running for 5 minutes:
![image.png](/.attachments/image-9a458b0e-0807-4928-a054-cd3c611618f5.png)

Step 5- The ML.Net creates a Zip file of the trained model that needs to loaded for further prediction.

Step 6- The Dockerfile created is now build and pushed to ACR.

Step 7- Create a VM and pull the image from ACR and hit the API for predictions. 
