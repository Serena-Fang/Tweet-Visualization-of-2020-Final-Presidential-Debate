# Tweet-Visualization-of-2020-Final-Presidential-Debate
Visualize tweets during final round of 2020 presidential debate in D3. Plot interactive word cloud, topic modelling scatter plot, dynamic pie chart, keyword evolution and bar chart.

Group Members: Serena Fang, Tracy Hu, Jessica Ji

The final presidential debate happened on October 22, 2020, 9:00 PM EDT. We used Tweet API to randomly scrape 12,000 tweets with tags like #debate, #president, #trump, and #biden from Oct.22 2020 3:00 PM to Oct.23 11:59 PM to analyze the evolution of tweet data. The resulting datasets are tweets_22/23sample.csv. Among the 32 attributes in the dataset, we focus mainly on text (tweet content), created time, source, and language. We also performed data preprocessing and generated topics.csv, prep2_tweets_2223.csv, tweets_words*.csv, time.csv, which are used for Figure 1-4, respectively. 

<img width="1017" alt="Screenshot 2021-12-10 at 12 33 04 PM" src="https://user-images.githubusercontent.com/73702692/147308581-e78582e2-eb2a-4fe6-8020-56f8851ddc5e.png">

Figure 1: This is an interactive scatter plot of top 50 topics from our selected tweets. Each circle represents a topic. The size of each circle is proportional to the topic frequency (adjusted to log scale). The most frequent topic appears on top left and the less frequent ones on bottom right. When mouseover a single circle, the circle will be highlighted in yellow, and a text with topic and count will appear. 

<img width="681" alt="Screenshot 2021-12-23 at 9 30 35 PM" src="https://user-images.githubusercontent.com/73702692/147308734-23d7a223-01c3-44d1-a93d-ef4dc3e279fb.png">

Figure 2: This bar chart shows the amount of tweets that each candidate was mentioned during each hour from Oct 22nd 3pm to Oct 23rd 11pm, with red representing Trump and blue representing Biden (same for word clouds). The bar will be highlighted and a text box with candidate name and tweet counts will appear when mouseover. The color opacity is scaled based on the frequency that a candidate is mentioned. 

<img width="783" alt="Screenshot 2021-12-23 at 9 30 46 PM" src="https://user-images.githubusercontent.com/73702692/147308782-706691d3-3ad9-4577-9892-eb9e940f497b.png">

Figure 3:  Each word cloud shows the top 50 high frequency words in the tweets that mentioned the two candidates. Commonly used words are larger and brighter in color, and vice versa. Tweets that mentioned both Trump and Biden are included in both datasets. 

<img width="1233" alt="Screenshot 2021-12-10 at 12 37 20 PM" src="https://user-images.githubusercontent.com/73702692/147308724-05d835ed-31b5-4faf-bc36-d991138ac214.png">

Figure 4: This interactive line chart shows the frequency evolution of the 9 representative keywords during the 33 hours (trump, donald, biden, joe, president, debate, hunter, vote, people). The x-axis represents the hours and the y-axis indicates the amount of tweets the word appears in. When mouseover, the area will be highlighted and the keyword will appear on the top left. 

<img width="819" alt="Screenshot 2021-12-23 at 9 30 59 PM" src="https://user-images.githubusercontent.com/73702692/147308847-ef01e3b8-582e-4e0e-8e52-af965b0d8a64.png">

Figure 5: These are two interactive pie charts: the left showing distribution of language (other than English) and the right showing distribution of sources of the Tweets. When clicking on the date button at the bottom left corner, the pie charts regarding the selected date will show. 

# Team Member Contribution
Serena
-scraped the dataset using Tweet API
-preprocessed text data (tokenization, topic modeling)
-produced topic modeling scatter plot
-produced two pie charts
-produced word evolution

Tracy
-preprocessed two datasets using python
-implemented the interactive bar chart
-helped with debugging the time evolution and added it to the final webpage

Jessica
-preprocessed text data (tokenization)
-produced the word cloud
-helped with the interaction between two pie charts
-integrated all the figures into the final webpage
-hosted the webpage and wrote system code document


# Reflection
We had ambitious plans at previous milestones, and we are happy that we accomplished most of them. It’s difficult to manipulate unfamiliar functions in D3 to adjust our graphical needs. The integration of all the figures into the final interface is also challenging. Building interactions between charts requires additional data processing within and outside of D3 and some figures use different versions of D3. In our initial plan, we hope to include an interaction between timeline and word cloud for tweets presented in that time period. However, we found that in order to do that, we have to store the word count data in a separate .csv file for every time period, which might be too burdensome and unnecessary in terms of memory, so we decided to produce one word cloud for each candidate. The team worked well together and the team is very collaborative. Every team member has an equal share of tasks that they are in charge of, meanwhile, each group member helps with each other when someone encounters difficulties. Despite the difficulties, the final visualizations were beyond our expectations as we put time and attention. We added the two additional interactive pie charts shown in Figure 5 that are not included in our initial plan since we want to display more data contents with meaningful interactions.
