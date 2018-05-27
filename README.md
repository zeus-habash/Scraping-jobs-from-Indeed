# Please read before runnnig the code
## Purpose of this code

I wrote this code for a project for the School of Management at the University of San Francisco. The purpose of the code was to be able to get a Dataset that captures different jobs posts from Indeed that can be analyzed to understand the job market demand, in terms of job titles, skills, industries and locations.

## The code structure:

1. Importing needed packages.

2. Loading CSV files that are the inputs for the code, the files contain the job searches and keywords you are looking for in each job.

3. Phase 1 - Sraping Job links: This code will create a dataset of all the job searches with links for each job.

4. Phase 2 - Scraping the body of job posts: This code will pull the body text of each job in the created dataset.

5. Phase 3 - Text mining the body of job posts: This code will look for the desired keywords and min years of experience needed for each job.

6. Phase 4 - Classifying jobs: This code classifies the jobs into different categories: Job title, Business Function / Department, and city.

## What to do with the searches and keywords CSV files:

These files act as inputs for the code, to make it easier to edit based on need.

You should edit your searches and desired keywords based on your need before running the python code.

### searches.csv:

This file contains the desired searches needed to be scraped from Indeed:
There are 4 columns:

1. Job Title: The job title you want to search for.

2. Job Location: The location you want to search for jobs in.

3. search radius (in miles): the radius of your job search.

****Note: It is better to have a small radius for different nearby cities, because Indeed limits you to 1000 results for each search.****

4. Job Type: You choose the desired job type in this field (fulltime, parttime, contract, commission, internship, temporary, all.)

### keywords.csv:

This file contains the desired keywords that you want to check if they are mentioned in the body text of each job post. The results for each keyword will be shown in a binary format ('1' if the word exists in the job post, '0' if the word does NOT exist in the job post.)

#### Things to know about keywords.csv:

1. Each keyword in this file will become a a binary variable in the final dataset.

2. Each column in the CSV file represents a category of keywords (e.g.: Soft Skills, Analytics Skills, Programing Languages.) The header of the dataset has names of each category, so that the user can easily know what are the different categories of keywords.

3. The second row in the dataset has acronyms for each keyword category, these acronyms will become prefixes for the keywords when they are appended in the final dataset, to keep the keywords' variables nice and clean to find and use.

4. You can add as many categories as you want, just make sure you follow the same format as the file shared in my repository and read the guidelines. 

## Things to know while running the code:

1. The code might take a long time to excute depending on the amount of job searches needed, however the code will show you the progress made while it is running, so you can sit, relax, or even run the code and go to sleep and come back later to see the results.

2. The code will track time needed for each phase in the code, and will give you a summary at the end of Phase 4. 
Here is the summary I got after I ran the code for my 1240 job searches:

##### Phase 1 took 02:00:17
##### Phase 2 took 02:19:51
##### Phase 3 took 00:04:45
##### Phase 4 took 00:00:15

##### The code ran for 04:25:11

3. Several job searches will show duplicate job posts, but do not worry the code will filter duplicate jobs twice: 
First after Phase 1: Removing jobs with the same job link.
Second after Phase 2: Removing jobs with the same job body of text. 

## Other uses for this code:

Me and many of my friends have used this code for our job search, we would edit the job searches based on what we are looking for, and input keywords of skills that we have and want to find jobs that are looking for these skills.

We would access the final dataset and filter the jobs to ones that match the skills/keywords that we want, and would have a list of jobs that exactly match our skillset, then we simply click on links of these jobs and apply.

## Project Contributors

### Vijay Mehrotra: 
#### Professor of Business Analytics & Information Systems at the University of San Francisco.

Professor Mehrotra was the project supervior for this project, he shaped the scope and timeline for this project, and provided the team with feedback and guidlines to acheive the project's goal in a timely manner.

Linkedin Profile: https://www.linkedin.com/in/vijay-mehrotra-ba9498
## 
### Zeus Habash: 
#### Talented Business Data Analyst with 8 years experience in various business functions. Has a strong ability to bridge the gap between the technical and the business sides, having a strong skill set in analytics and its translation into actionable insights, decisions, and recommendations.

Zeus Habash is the author of this README, I wrote the code and documentation for this project on Python, and made sure that the program meets the guidlines of Prof. Mehrotra, and colaborated with Joaquin Hernandez to reach our goal of maximizing the utilization of this program to be as beneficial to as many stakeholders as possible. I also made sure that this code can be understood, used, and edited by any pythonista.

Linkedin Profile: https://www.linkedin.com/in/zeus-habash

Website: https://zeushabash.com
##
### Joaquin Hernndez: 

#### HR professional with 7 years experience in various HR functions including but not limited to recruiting, talent acquisition, People analytics, and HR systems.

Joaquin Hernandez was the subject matter expert in this project. He provided the team with the job searches needed to acquire our desired dataset. He also identified keywords and metrics needed for the analysis of the dataset. Last but not least, worked on the logic of classifying the jobs into fewer job titles categories, and different business functions.

Linkedin Profile: https://www.linkedin.com/in/joaquin-hernandez-43b9b795

Website: https://iamjoaquinhernandez.com
##
#### Thank you for reading, enjoy running the code! 
#### Please feel free to contact me if you need any help, looking forward to hearing your comments.
