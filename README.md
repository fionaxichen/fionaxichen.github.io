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

*Code:*
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

*Code:*
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

## Result and Visualization:

![image](https://user-images.githubusercontent.com/120151846/206618571-7d851bf7-a7a0-4e76-94bd-2bf55009d868.png)
![image](https://user-images.githubusercontent.com/120151846/206618601-b9542606-5400-4077-b689-d908b034bbd5.png)
![image](https://user-images.githubusercontent.com/120151846/206618640-70c5f88d-ab93-4543-9290-759f211a1783.png)


# Project 2: Shopper Hiring Problem Project (Used BigQuery SQL and Tableau)

## Context
In this simulated dataset, we have been running an A/B test on our shopper hiring funnel to see if initiating the required applicant background check earlier in the process would improve conversion rates. The theory is that shoppers will maintain their momentum and be more likely (and start more quickly) if the required prerequisites are completed faster. <br>
The background check costs us $30 to complete. A shopper must both activate the prepaid debit card we mail to them (to use when paying for groceries purchased for our customers) and have successfully passed their background check to complete their first batch of orders. Completing the online orientation, however, is optional. <br>
In this scenario, “success” for our shopper recruiting funnel is achieved if they complete their first batch (see “first_batch_completed_date”)

## Question #1: Based on this data. What can we conclude at this point from the A/B test (in which we tried initiating the background check earlier in the hiring process for the treatment shoppers)? And how confident should we be in this conclusion?

Null hypothesis: no difference between control and treatment groups <br>
Alternative hypothesis: control group and treatment group are different <br>

I am 95% confident that the true mean of success is between (0.19799, 0.198). Since 19.799% is much greater than 0%, we can reject the null hypothesis. <br>

Thus, we can conclude that initiating the background check earlier in the hiring process is effective.

![image](https://user-images.githubusercontent.com/120151846/206619891-f5a82098-d6e9-4706-b929-c89abb4b82af.png)
![image](https://user-images.githubusercontent.com/120151846/206619935-f79b788e-671b-4e02-8415-635e286a2a7d.png)

## Question #2: We’d like to know if this change is cost-effective. How should we think about the cost-effectiveness of this change? Please be as specific as you can here.

In this case, the average cost per first batch completion is the most effective metric to evaluate whether this change is cost-effective or not. <br>

Based on the Tableau chart, we can see that cost per first batch completion for all four channels have reduced when we initiate background check earlier. It is especially cost-effective for job search site channel, shopper referral bonus channel, and web search engine channel. <br>

The reason for social media channel’s lower reduction in cost is that people who use social media to start this application are likely not very serious about job hunting, for they passively click on the advertisement instead of actively looking for a job by using channels such as job search sites.

![image](https://user-images.githubusercontent.com/120151846/206620172-3b34aa98-1fea-4138-b81e-399d0a331ff5.png)
![image](https://user-images.githubusercontent.com/120151846/206620200-557aa134-e790-4ec8-b2ac-718aa8403c8f.png)
![image](https://user-images.githubusercontent.com/120151846/206620246-c0f52c34-96d2-4c18-99b9-66b966f0f3e0.png)

## Question #3: What other observations and recommendations do you have for us, based on this data? (for example, what else did you find that seems relevant, or what else would you want to test if we ran an additional experiment?)

Observations:
1. Job search site channel
  - Lowest conversion rate in the control group
  - Conversion rate will significantly improve if initiating background check earlier
2. Shopper referral bonus channel
  - Higher conversion rate in the control group
  - Conversion rate will significantly improve if initiating background check earlier
3. Social media channel
  - Highest conversion rate in the control group
  -  Initiating background check earlier will not significantly improve conversion rate
4. Web search engine channel
- Lower conversion rate in the control group
- Conversion rate will significantly improve if initiating background check earlier

![image](https://user-images.githubusercontent.com/120151846/206620882-3794745d-3c4b-4712-877c-7f2f851b738b.png)

Recommendations:
1. The conversion rate in social media channel’s treatment group did not improve very much. One reason is that its conversion rate in the control group is already the highest. However, even with such high control conversion rate, its treatment conversion rate is actually the lowest among the four channels. Therefore, we could evaluate the ROI of both control and treatment groups, which is channel advertising cost + $30 background fee. If treatment ROI is larger than that of the control group then we should initiate background check earlier. If it is smaller than its control group, then we should not initiate early.
2. Perform another A/B Test to evaluate if mandatory orientation could improve the conversion rate.

# Project 3: User Engagement Analysis Project (Used DBeaver PostgreSQL and Tableau)

## Context
User dataset event.csv and email.csv to analyze why the user engagement, which is the number of logins, decreased last month.

## Solution
Users can be separated into two segments: existing users and new users
- Based on the data provided in the email.csv, we can conclude that when event_type = signup_flow, the corresponding user id belongs to a new user since you have to complete signup before trying to login.

We can first analyze new users
- event_type = signup_flow has additional four steps under event_name. To find out the order of these steps, we can check their number of users in each step. Larger the number of users, earlier the step. Based on the result:

***create_user  —>  enter_email  —>  enter_info  —>  complete_signup***

![image](https://user-images.githubusercontent.com/120151846/206622226-94d11064-90c7-4aca-a466-bef6a4fae32c.png)
![image](https://user-images.githubusercontent.com/120151846/206622258-8ff2b568-6a34-4957-89e8-5a72ae15f856.png)

- I used funnel analysis to analyze the four steps: calculate the number of users who have converted through each step of the funnel. After entering email, the conversion rates do not have a severe drop-off of user.

![image](https://user-images.githubusercontent.com/120151846/206622397-b4f98475-2df3-484f-8e4a-c454d5173b2f.png)

- Below we can see that the trend for all four steps is relatively constant, which is high during the week and low on weekends. Since this trend is normal, it is possible that the dip in user engagement is coming from existing users as opposed to new users.

![image](https://user-images.githubusercontent.com/120151846/206622477-e00bcc42-3984-4a18-ae4e-016290961e10.png)

Engagement also includes new users
- Analyze user lifetime using retention analysis: 
  * It shows user lifetime is around 20 weeks. 
  * This means most of users will churn in 20 weeks after they first signup.

![image](https://user-images.githubusercontent.com/120151846/206622615-115e7546-3955-4f3f-aff2-d7017688f855.png)

- Analyze devices including computers, phones, and tablets: 
  * There is a steep drop in both phone and tablet engagement rates. 
  * It is likely that there’s a problem with phones and tablets related to the long time user retention

![image](https://user-images.githubusercontent.com/120151846/206622684-09f5f88f-6462-480d-9d72-d1295de02782.png)

- Analyze emails and email clickthrough rate
  * Email sent = number of weekly digest + number of re-engagement emails
  * Clickthrough rate plummeted, indicating clearly that the problem has to do with emails in addition to devices

![image](https://user-images.githubusercontent.com/120151846/206623551-efaab95e-2cf0-4ede-b739-d066a6a21f34.png)
![image](https://user-images.githubusercontent.com/120151846/206623588-9feecaf8-df57-4acc-8d25-5908fed3abb2.png)

## Recommendations

After investigation, it appears that the problem has to do with devices, including phones and tablets, and emails. <br>
- Next step:
  * Notify the Product Manager that phone and tablet apps have problems, and email links might not be working properly
  * If email links work then communicate with the marketing team to check all the email templates sent last month
    * The template might not be intriguing enough to attract users to click these emails



