# Nextgrowthlab-task
Nextgrowthlab Jr data scientist task

Question 1:

Write a regex to extract all the numbers with orange color background from the below text in italics. {"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}

Question 2:
From chrome reviews, goal is to identify such ratings where review text is good, but rating is negative- so that the support team can point this to users. Deploy it using - Flask/Streamlit etc and share the live link. Answer: Idea -

Read the data from CSV file using pandas .

Extract the necessary columns ( text, star and thumbs-up .)

Convert the text into lower case letters and remove the punctuations using backspace.

Sentiment analysis using textBlob :- find the polarity and subjectivity of the text and add both in seperate columns.

Lets consider polarity >0.3 is Posivie and polarity <= -0.3 Negative and subjectivity > 0.5 is strongly support with this we have Strongly Positive, Positive, Neutral , Strongly Neutral, Negative, Strongly Negative

Add a new column to show the sentiment of the text .

Extract the strongly positive and positive text with 1 star rating .

Plot the graph using the data . Looking at the plot we can easily say people with neutral comment even gave very high 1 star rating People with very good positive rating few people gave 1 star very few people with moderately positve rating gave 1 star on an overall There are 81 number of ratings with positive comments but with low rating There are 250 number of ratings with Neutral comments but with low rating

Q3. Part 2 (Two Questions) Check if the sentence is Grammatically correct: Please use any pre-trained model or use text from open datasets. Once done, please evaluate the English Grammar in the text column of the below dataset.

Answer : Steps used :

Read input data from csv using pandas

Extract the relevant columns only

pass each comment to language tool and check for grammar correctness

If correct do nothing - mention No mistakes

If incorrect - as shown by the match count, mention mistakes found
Output is again a csv - with column 1 being text and column 2 being the number of mistakes in the text

Sample output
Tony bahut funny hai Hill climbing racing my favourite game -- Mistakes found, 3 mistakes Teturwu -- Mistakes found, 1 mistakes Hoooooooooooyaaaaaaaaa what a game hooooooooooooyaaaaaaaa -- Mistakes found, 2 mistakes This game is nice -- No mistakes Rahulyadavo -- Mistakes found, 1 mistakes Very taty -- Mistakes found, 1 mistakes good -- No mistakes I LIKE THIS GAME -- No Mistakes

