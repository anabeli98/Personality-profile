# INTRODUCTION

¿How important is Healthcare? ¿And Mental Health?

I suppose that all of us would like to have the best medical attention, with a huge group of specialist and medical devices taking care of our heatlh, but sometimes the economy doesn´t allow this. 

Now imagine that thanks of AI we could develop a tool that can help medical specialist to detect patients´ psychological profile.

This tool could be used, for example, when patients need a long treatment or have a chronic disease. The specialist could obtain the psichological profile at the begining of the treatment, and then analyze their evolution to detect some alerts such as depression or another sign of mental illness.

---

During my final thesis of my bachelor degree I used 2 neural networks to develop a tool which can get conection to public profiles of Twitter, download all their tweets (without RT) and process them to obtain an infographic of the psychological profile of the accounts based on their personality (according to the Big5 classification) and their main emotions.

### Materials:

- Model developed by IBM (IBM Watson Personality Insights) that obtain personality classification according to the Big5 classification when it process long text
- Model developed by a UPM student that classify tweets according to the main emotion it expressed
- Twitter API to generate de conection between Twitter and Python
- Different libraries such as TensorFlow, to work with deep learning

### Steps:

- Import Dependences
- Get Data from Twitter
- Emotional Analysis
- Personality Insights Analysis
- Generate an Infographic
- Send documents via Email


#### Get Data from Twitter:

Specific account (Twitter for Developers) and specific credentials are needed to could use Twitter APIs.

Download relevant info of the account, and tweets since date of creation.

Create a dataframe with different columns. One of them will be used to obtain the personality analysis, another to obtain the wordclouds and another to obtain de emotional analysis.

#### Emotional Analysis:

Import the pre-trained model (it is called "model.h5")

Use the model with the correct colum of the dataframe and include the results in a new colum

- Wordcloud:
Create a wordcloud of each emotion (we need a specific dataframe of each emotion)
Choose color and form of each wordcloud
Obtain different text for each wordcloud

- Emotional evolution:
Create a dataframe that counts de number of tweets per month
Create a new colum that count the number of tweets of each emotion per month
Obtain 6 graphics. One for each emotion. Each graphic show the evolution of that emotion 
Obtain a joint graph (a stacked bar chart plot)
The joint graph is a stacked bar chart plot. The graphic represent the whole account

    * In this part we could obtain different graphs to analyze emotion evolution for example throught the Covid-19

#### Personality Insights Analysis:

Import the IBM model

Specific account in IBM Cloud and specific credentials are needed to could use IBM programs

Generate the text that will be used in the model

Visualize the results of the Json obteining different graphics: Needs, Values and Big5 classification

Generate a joint graphic with Big5 classification and their subcharacteristics

#### Generate an Infographic:

Is a personalized infographic that show the main conclussion about the needs, values and personality of the account.

Generate the different texts that will be include in the infographic

Transform the "int" into "string" to could mix in a sentence

Choose what text will be used according to the most representative data

Define the sizes of the infographic and choose the location of the data

#### Send documents via Email:

You need to give permission in myaccount.google.com for insecure apps to have access to gmail

You need to download a MIME (Multipurpose Internet Mail Extensions). 
This is necesary for smtplib to accept other characters appart from ASCII (such as images or pdf)
