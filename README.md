# Scraping jobs from Indeed
## Purpose of this code

I wrote this code for a project for the School of Management at the University of San Francisco. The purpose of the code was to be able to get a Dataset that captures different jobs posts from Indeed that can be analyzed to understand the job market demand, in terms of job titles, skills, industries and locations.

## The code structure:

1. Importing needed packages.

2. Loading CSV files that are the inputs for the code, the files contain the job searches and keywords you are looking for in each job.

3. Phase 1 - Sraping Job links: This code will create a dataset of all the job searches with links for each job.

4. Phase 2 - Scraping the body of job posts: This code will pull the body text of each job in the created dataset.

5. Phase 3 - Text mining the body of job posts: This code will look for the desired keywords and min years of experience needed for each job.

6. Phase 4 - Classifying jobs: This code classifies the jobs into different categories: Job title, Business Function (department), and city.

## What to do with the searches and keywords CSV files:

These files act as inputs for the code, to make it easier to edit based on need.

You should edit your searches and desired keywords based on your need before running the python code.

### - searches.csv:

This file contains the desired searches needed to be scraped from Indeed:
There are 4 columns:

1. Job Title: The job title you want to search for.

2. Job Location: The location you want to search for jobs in.

3. search radius (in miles): the radius of your job search.

**Note: It is better to have a small radius for different nearby cities, because Indeed limits you to 1000 results for each search.**

4. Job Type: You choose the desired job type in this field (fulltime, parttime, contract, commission, internship, temporary, all.)

### - keywords.csv"

This file contains the desired keywords that you want to check if they are mentioned in the body text of each job post. The results for each keyword will be shown in a binary format ('1' if the word exists in the job post, '0' if the word does NOT exist in the job post.)

#### Things to know about keywords.csv:

1. Each keyword in this file will become a a binary variable in the final dataset.

2. Each column in the CSV file represents a category of keywords (e.g.: Soft Skills, Analytics Skills, Programing Languages.) The header of the dataset has names of each category, so that the user can easily know what are the different categories of keywords.

3. The second row in the dataset has acronyms for each keyword category, these acronyms will become prefixes for the keywords when they are appended in the final dataset, to keep the keywords' variables nice and clean to find and use.

4. You can add as many categories as you want, just make sure you follow the same format as the file shared in my repository and read the guidelines. 

##
