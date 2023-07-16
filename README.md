# nosql-challenge
Module 12 challenge using MongoDB and NoSQL databases

## Introduction/Premise

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Summary

The NoSQL_setup Jupyter Notebook connects to MongoDB and then imports the database of UK Food establishments from the establishments json file, which has been loaded into MongoSH with the following code:

`mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`

This file also loads the new restaurant, updates it, removes some entries and changes some of the variable types from the raw data.

The NoSQL_analysis Jupyter Notebook then explores the data using pymongo to answer five questions:

1. Which establishments have a hygiene score equal to 20?

There are 41 establishments with a Hygiene score of 20.

2. Which establishments in London have a `RatingValue` greater than or equal to 4?

There are 33 establishments with a rating of at least four in London.

** Please note this result is different than rubric, but I contacted AskBCS team and was told the rubric is wrong and that 33 is the correct answer. **

3. What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

Volunteer, Plumstead Manor Nursery, Atlantic Fish Bar, Iceland, Howe and Co Fish and Chips - Van 17.

4. How many establishments in each Local Authority area have a hygiene score of 0?

There are 55 Local Authority areas in the data and a dataframe is created showing how many establishments have a hygiene score of 0.

## Modules

pymongo

pprint

pandas

As well as the MongoDB infrastructure, including MongoSH and the Mongo import client.

## Citations

Used one piece of code from outside class to test the variables at the end of the first notebook.

https://www.w3schools.com/python/ref_func_isinstance.asp