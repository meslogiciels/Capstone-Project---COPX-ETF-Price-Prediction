# AWS Machine Learning Engineer Nanodegree
---

## Capstone Project - Global X Copper Miners ETF Price Prediction

### Project Overview
Since 2021, inflation in the United States of America has increased dramatically. Indeed, from 1.2% in 2020, the US inflation rate rose to 6.8% at the end of November 2021, its highest since 1982.

In these uncertain times, for those of us who have a stake in the stock market, how do we protect our investments from the negative impacts of inflation? We do by investing in assets that performs well during inflationary periods.

Historically, copper is one of the best performing assets during inflationary periods. As a result, predicting changes in the value of copper has obvious financial benefit including knowing when to buy or sell.

Using historical stock prices for the Global X Copper Miners Exchange Traded Fund (ETF), that we obtained from Yahoo! Finance, we created three machine learning models tasked to predict the next day's closing price for copper.

The three models that I used were a Linear Regression model, a Random Forest model and a Long Short-Term Memory model. By comparing the capabilities of our models to predict the ETF next day's closing price, we were able to determine that our first model (the Linear Regression) would be the model to be deployed.

### Project Implementation
This project created and completed using Amazon SageMaker (a cloud based machine-learning platform launched in November 2017).

Completing this project requires access to an Amazon Web Services (AWS) account. For those of us interested, Amazon does offer a <a href="https://aws.amazon.com/free/" target="_blank">Free Tier</a> account.

#### Project Requirements
1. An 'AWS' account.
2. An 'S3' bucket and a 'train' sub-folder to upload the project's data.
3. A 'SageMaker Notebook Instance,' a machine learning (ML) compute instance running the 'Jupyter Notebook' App.  
To create a 'SageMaker Notebook Instance', one must do the following:

   - Log into one's AWS management console;
   - Go to the SageMaker service;
   - In the left navigation panel, under 'Notebook,' select 'Notebook instances;'
   - Configure the Notebook instance by setting the 'Notebook instance type' to 'ml.t2.medium.' A choice perfectly suited for our purpose.
   - Create the instance via the 'Create notebook instance' button at the bottom of the page.
   - It might take a few minutes for the instance to be created. Once it has been created, it will be listed within the 'Notebook instances' dashboard.
4. A 'Jupyter Notebook,' an open source web application that one can use to create and share documents that contain live code, equations, visualizations, and text.
To create a 'Jupyter Notebook', one must do the following:

    - Select the newly created 'SageMaker Notebook Instance.' If it is not currently in service, start it and wait for its status to be 'InService.'
    - To the right of the 'SageMaker Notebook Instance' that is now in service, click on the 'Open JupyterLab' hyperlink to launch 'JupyterLab.'
    - In the left sidebar, choose the **File Browser** icon ( ![](Report%20-%20Images/FileBrowserIcon.png) ).
    - Choose the root folder.
    - In the left sidebar, choose the **Git** icon ( ![](Report%20-%20Images/GitIcon.png) ).
    - Choose **Clone a Repository**.
    - Enter the URI for this repository.
    - Choose **CLONE**.
    - Wait for the download to finish. After the repository has been cloned, the **File Browser** opens to display the cloned repository.
    - Open the `copper_price_predictor-EMAs.ipynb` Jupyter Notebook.

We are now ready to run the code found in our newly opened Jupyter Notebook.

To run the code, simply execute each cell, but the last one, one by one, from top to bottom. To run a cell, we have the option to click on the **Play** ( ![](Report%20-%20Images/PlayIcom.png) ) icon or the <Shift><Enter> keys on the keyboard.

When all the cells, but the last one has been executed, you will have deployed a Linear Regression model on AWS SageMaker.

#### Warning
Running a 'SageMaker Notebook Instance' and deploying a machine learning model will incur costs. In order to minimize these costs, do NOT forget to run the last cell of the Jupyter Notebook. Executing this last cell will delete the model endpoint and ending its cost.

Finally, the 'SageMaker Notebook Instance' currently in service must be stopped.

### Files in this Repository
* `copper_price_predictor-EMAs.ipynb`, the Jupyter Notebook needed for this project;
* `stock_market_data-COPX.csv`, the historical stock prices for the COPX ETF;
* `Proposal.pdf`, the proposal for creating this project;
* `Report.pdf`, a report detailing the completed project;
* **Report - Images**, a folder holding the images associated with this `ReadMe.md` file.

### Conclusion
Obviously no project is perfect at first. The same goes for this project. Having more time and resources, we might have been able to achieve better accuracy. For example, if we keep in mind that the stock market is driven by more than historical stock prices, we might have been able to add a sentiment analysis based on external elements such as news about the economy, the perceived mood of the population to our project.