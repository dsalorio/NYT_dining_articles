# NYT_dining_articles

Natural language processing analysis of recipe descriptions in the New York Times dining section

## Project Description and Inspiration

I love the New York Times [Dining section](https://cooking.nytimes.com/).
I like to eat good food, thankfully I also like to cook, and I also really like to READ about cooking. 
This project, then, isn't about recipes themselves, but how we talk about them. I've taken the paragraph or two that chef-authors use to describe their recipes and performed some analysis using Natural Language Processing techniques to get a sense of what each recipe is like. I'm not examining the ingredients list for a recipe, or the instructions for making it. I'm looking at how people talk about it, describe it, what's it like to make it and eat it.

The workflow is split between 2 notebooks and is more or less as follows

* Start by scraping these recipe descriptions and dropping them into a Mongo database. 
* Clean and prep the text, removing stop words and using regexs. 
* Test various different stemmers and lemmatizers, as well as count vectorizers, from the NLTK and SpaCy libraries.
* Compare Latent Semantic Analysis, Non-Negative Matrix Factorization, and Latent Dirichlet Allocation models, from Sci-Kit Learn and Gensim, to generate topics.
* Settle on a champion workflow using WordNetLemmatizer to simplify my text, Tf-Idf Vectorizer to get my 'bag of words' sparse matrix, and Non-Negative Matrix factorizataion to generate topics.
* Use my final model and cosine similarity to create a recipe recommender.

If this is interesting have a look around the NYT's website, and if you like what you see buy a membership and support great journalism!

## Future Work

There is still a lot of neat stuff left to do with this data. I haven't looked at positional or semantic data, so word2vec and GloVe models in the Gensim library are the next place I'm headed. Somewhere down the line I will move on to Transfer Learning to really get the recipe recommender in top shape.

### A Note about Requirements, and a request for WSL help

I developed this code in an Ubuntu environment, and it should be hardy to most Unix and Linux environments. I'm trying to get it to work on WSL, but the folks at MongoDB say they don't support WSL, so that's holding me up. That said, I've seen somebody run Mongo on WSL! If you know how to get Mongo running on WSL, please reach out! 
