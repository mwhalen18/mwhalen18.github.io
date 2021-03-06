---
title: "MovieRec"
permalink: /projects/MovieRec
---

[Click here to see the bot in action!](https://twitter.com/rec_movie)

## Updates on robo-baby

  - 04-04-21: Twitter bot has a new learning algorithm, based on bag-of-words modelling (this replaces the previous 'what does Matt think the most important features are for predicting a movie' model)
  - 03-22-21: Twitter bot now recommends a random movie every day!
  - 03-02-21: Twitter bot now lives in the cloud!
  - 03-01-21: Twitter bot is down because my computer crashed :(

# About the project

Sometimes deciding what to watch is half the battle...

I love movies and I love `R` so almost immediately after discovering `R` I asked "what can I do with movie data"? I know now that there are dozens of great movie datasets including the movieLens and Kaggle TMDb datasets, both available for free. But these arent updated regularly, and I wanted to develop a pipeline to do soemthing interesting with up to date movie data.

While this project went through a few stages of early (aka bad) protoypes -- see [this godawful shiny dashboard I made]() -- what I enventually decided I wanted to do was make an app that can recommed movies. In due time I will outline here some of the process of building the app, but for now I will simply list my data sources, and link off to the source code and the bot itself (which isn't seeing nearly enough action). 

## The data

I wanted to be able to not only recommend movies, but also let users know which movies are available on what streaming services. Ina ddition to using the `TMDb` database for all of the actual movie information I also pulled streaming data from reelgood.com. Both of these datasets are automatically updated weekly to stay current. 

## The model

I intially started out with a self-specified model where I weighted actors and directors for each movie using a scientific method called 'personal opinion' -- again I made this before having ever heard of machine learning. All I did was generate similarity matrices for the director, actors, and genres, then wight each one using a 'best-guess' appraoch. The results weren't terrible but it'sobviously fairly unscientific. I have since updated it to use a bag-of-words cosine-similarity model. I could certainyl imprive upon this but it works fine for now...

> Although there is a weird bug where the model occasionally aggressively recommends the movie "Footloose"

## The bot

Once everything else was up and running the bot was easy! The rest was just automating the scripts and sitting back and watching it do its thing. I am effectively the only person who actually engages with the thing so I have also programmed it to tweet on its own every so often.

## Caveats

This was a fantastic first adventure into a solo data project. I learned a lot and looking back I wish I could spend more time improving it. I would love to throw other learning models at it or include additional variables in the cosine similarity, but I will leave it as is and just enjoy that one year after downloading `R` for the first time I made this little toy.

**Check out the bot in action!**

[@rec_movie](https://twitter.com/rec_movie)

**Link to the Github repo**
[Github -- MovieRecommender](https://github.com/mwhalen18/MovieRecommender)



