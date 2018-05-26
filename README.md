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

### searches.csv:

This file contains the desired searches needed to be scraped from Indeed:
There are 5 columns:

1. Job Title: The job title you want to search for.

2. Job Location: The location you want to search for jobs in.

3. search radius (in miles): the radius of your job search.
#### Note: it is better to have a small radius for different nearby cities, because Indeed limits you to 1000 results for each search.

