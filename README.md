# Travel Guide Chatbot
There are two ways to run this chatbot, the first one being easier and less time-consuming than the second. Both will result in our python code connecting to the dialogflow chatbot, but the first option is more stable than the first.

**NOTE:** We have already scraped knowledge bases for the following countries: United States, Canada, Mexico, Brazil, Argentina, United Kingdom, France, Germany, Italy, Spain, Russia, China, Japan, South Korea, India, Australia, New Zealand, Egypt, South Africa, Nigeria, and Croatia. We have implemented dynamic web scraping for other countries, but it will take a few minutes to scrape, and you may get errors during that time period.



## Option 1 - Recommended but requires local installation

### Installation process
1. Ensure nltk is installed. If not already installed, install nltk by running `pip install nltk`

    A. To further ensure all necessary packages are installed for nltk to not get runtime errors follow these steps:

        i. type in 'python' or similar to enter the python interpreter on your command line
        ii. type in import nltk
        iii. type in nltk.download(), select all and wait for a successful download
        
2. Ensure locationtagger is installed. Install it by running  `pip install locationtagger`

3. Configure the Google Cloud set up

    A. Install the [google cloud CLI](https://cloud.google.com/sdk/docs/install), by following the first two steps for your OS
    B. When prompted to enter google account details to access a project use the following. If you weren't prompted you can run this command gcloud auth application-default login
        email - nlpchatbotproject@gmail.com
        password - cs4395password
    select the only project listed under this account and that will complete the configuration of the google cloud
    
4. Run these 2 commands to install the final necessary libraries

    a. `pip install google-cloud-dialogflow`
    
    b. `python -m spacy download en_core_web_sm`

5. You can now run the chatbot by running `python chatbot.py` with your local python installation.

## Option 2 - Requires no setup, but is less stable
To allow for easy testing purposes, you can simply click on this dialog flow generated [link](https://console.dialogflow.com/api-client/demo/embedded/1ed112ff-ab5a-4e7a-96d4-dd4d7c29b09c) that will allow you to simply talk to to our chatbot running at this link. We have accomplished this by building a Flask web server that is integrated with Dialogflow via webhooks.

However, this option requires that we are actively running our Flask web server from one of our computers. Please message us before you attempt to run the project this way so we can ensure it is running for you. You can reach us on Discord at fasnow#7731 or cady#6453 (preferred for faster responses) or by email at fcd180001@utdallas.edu or cmb180010@utdallas.edu.

Additionally, there is the constraint that you should only mention a country's name once when you talk about it. Meaning, once you have told the chatbot what country you are interested in, you should not refer to the country by name again (e.g. do not say "What kind of food does Italy have?", say "What kind of food do they have?"). This is due to a constraint in how we can make webhook requests.

Note that this method of running our program is unstable due to webhook constraints imposed by the free version of Dialogflow.

## Sample phrases to ask our chatbot:
- I want to visit Italy.
- What kind of food should I eat there?
- I don't like pizza.
- What other meals can I eat?
- What should I do there?
- What should I see there?
- Actually, I want to visit France instead.
- What cities do you recommend?
- What languages do they speak?
- What is the local currency?
- How do I stay safe there?
- How is the weather in the summer?
- Thank you, goodbye!
