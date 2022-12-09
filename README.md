# Project 1: Hot News Lookup (Used Python and Natural Language Processing)

## Problem:
Currently, we are flooded with information from different media outlets. This flood of information hinders our ability to effectively follow the most relevant information. Given the sheer magnitude of information available, we do not have the time to read through every piece of news, or even their titles, to determine which ones are more important than others. Quickly distinguishing the substantial from the trivial is ever more difficult.

## Solution:
We will create a Flask app that gathers data on news from all over the world, all across the web, and processes them to calculate the importance of any keyword on a given day or over a period of time. The program would be able to show you how important a topic (keyword) is and provide news articles that are related to the topic.

## Potential Uses:
1. Journalists monitoring news and tracking the trend of a certain recent news topic
2. Public browsing daily news in a more quick and effective manner
3. Institutions/individuals looking up themselves to manage their public image and level of discussion

## Function 1: Everything
Allows users to input a keyword using its API parameter “q” <br>
Searches through articles from over 80,000 large and small news sources and blogs <br>
Return articles that contain the keyword <br>
Code:
  - Get the time range using datetime 
  - Extract data for all news articles from News API with the parameters
  - Extract data from News API that contains user’s keyword
![image](https://user-images.githubusercontent.com/120151846/206617246-67a0f938-094a-4736-8fa2-a00633e6e766.png)
![image](https://user-images.githubusercontent.com/120151846/206617408-13947833-3e16-4a38-947e-4c6079ebac21.png)

  - Calculate the popularity
  - Transfer data from Json into lists using for loops
![image](https://user-images.githubusercontent.com/120151846/206617522-eb1823bb-8683-4715-98ed-433bd909f834.png)

  - Create a table that contains: Title, Published date, Description, Source, 
  - Return the popularity of the keyword and table of related articles’ information
 ![image](https://user-images.githubusercontent.com/120151846/206617821-0f558f8a-ede3-4ff2-bafb-45f06ec8ed49.png)
 
## Function 2: Top Headlines
Search through top headlines from 40 countries <br>
Conduct natural language processing for top headlines across global sources <br>
Identify the most popular keywords worldwide <br>
Code:
  - Choose countries that we want to get the information from and create columns that we need.
 ![image](https://user-images.githubusercontent.com/120151846/206617974-64603f74-006a-49eb-b16a-75c6d6caaed7.png)
 ![image](https://user-images.githubusercontent.com/120151846/206618036-525bc2e7-350a-45cf-9682-209ceed067e6.png)
 
  - Tokenize and lemmatize words, including cleansing the text of special characters; returns a lemmatized list
![image](https://user-images.githubusercontent.com/120151846/206618111-4402a141-d9e8-47b6-925f-2f360566e681.png)

  - Get rid of all stop words, returns a word list without any stop words
![image](https://user-images.githubusercontent.com/120151846/206618190-132842e2-b9df-405f-bc3f-d7b9439d88cc.png)

  - Generates a dictionary using word and frequency lists to count occurrences of words in headlines
 ![image](https://user-images.githubusercontent.com/120151846/206618287-b56b36d7-5ff6-4cb8-8204-b708628fee96.png)
 
  - Run a news title processing from the beginning to end; returns a dictionary with word and frequency
![image](https://user-images.githubusercontent.com/120151846/206618357-f7d4c995-e22e-4577-baf5-d605cbb90f83.png)

  - Run all defined functions, sort the word list, and generate word cloud visualization
![image](https://user-images.githubusercontent.com/120151846/206618411-8adb98b1-dfd9-4841-bfc2-882dd0a6d919.png)

![image](https://user-images.githubusercontent.com/120151846/206618458-07d399e1-11af-43f2-b2f9-3e82094860d8.png)

Result and Visualization:
![image](https://user-images.githubusercontent.com/120151846/206618571-7d851bf7-a7a0-4e76-94bd-2bf55009d868.png)
![image](https://user-images.githubusercontent.com/120151846/206618601-b9542606-5400-4077-b689-d908b034bbd5.png)
![image](https://user-images.githubusercontent.com/120151846/206618640-70c5f88d-ab93-4543-9290-759f211a1783.png)







