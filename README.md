# IDP
This repository contains the source code file along with the link to the csv data set I have used to build the prototype for my inter-disciplinary project.

The topic chosen for the Inter-Disciplinary project is : An AI Automated Personalized Itinerary Generator For Remote Places

My approach to building this project:
- Select a data set of travel destinations to train a recommender algorithm.
- Train the recommender algorithm.
    - The recommender works based on two parameters : Similarity Match and Sentiment Score
    - Similarity match : Calculated using SpaCy's en_core_md model. It tokenizes the reviews from users and finds the similarity between the required attributes and          the attributes of each place to rank them by similarity score.
    - Sentiment Score : Calculated using the Vader Sentiment Analysis NLP. It provides a Normalized Sentiment Score for each place based on tokenized user reviews.
    - An Aggregate score of the two parameters is calculated to find match percentage : the best sentiment score and most similar get ranked on top, and the rest            follow.
    - Based on the final match percentages, the user is given multiple recommendations, and with each recommended destination, a set of other similar places in the          vicinity.
- Itinerary generator : currently, the itinerary is generated using gemini api for the gemini 2.5 flash model. it takes the outputs given by the recommender algorithm to search the internet for best prices and make a perfect plan. Future prospects include developing our own System for Itinerary generation with a dataset of prices, accomodations, etc.
- Testing : The testing is done on a data set of remote places which will be collected through web scraping. The dataset will then be preprocessed and filtered. Then it will replace the existing dataset of destinations.
- The inputs for testing will be generated from a dataset that contains a public survey's responses about what kind of location they would like to visit.
