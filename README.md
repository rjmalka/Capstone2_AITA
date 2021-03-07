# Capstone2_AITA

Robert Malka
Springboard Data Science Career Track, March 2020 cohort

Capstone Project II

### Problem Statement: 

What features might serve to better predict whether or not an individual is behaving like an asshole, and how can we optimize a model to best use those features?

### Background:

How do people perceive what we’re saying and why? Are there any qualities about our tone, word choice, and phrasing that would make someone like us less, think better of us, or carry our message across with further clarity? If we could find answers to this question by sifting through aggregate data, we might be better able to convince a judge/jury that we’re not at fault, create a more effective business pitch, or, for the field of self-help, help others be more persuasive. 

Shifting away from the narrow perspective of business value-add, we can also examine the limits of machine learning’s understanding by means of this dataset – examining where machine learning, and the current state of AI generally, falls (far) short in its assessment of e.g. a person being (or not being) an asshole. Insofar as this can be shown through this project, we validate the value and uniqueness of being human.

### Data Source:

My data was received, largely clean, from: https://github.com/iterative/aita_dataset. The data was about 97,000 rows.

### Features:

Basic facts about the dataset
The basic features of the dataset are:
•	id: The unique post ID
•	timestamp: The timestamp of the post in datetime (originally in epoch time)
•	title: The subject line of the post
•	body: The full body of the post
•	edited: Whether it was edited or not (T/F)
•	verdict: The community's decision ("You're the Asshole" and "Everyone Sucks" both count as being an asshole)
•	score: The number of "upvotes" the community gave to that post (roughly, how much interest the community had in that post)
•	num_comments: How many people commented on the post
•	is_asshole: 1 for yes, 0 for no

Of the body and title features, I developed core features to examine:
•	countI: How many times I is said in the body of the text. (Does number of "I"s correlate with narcissism/being an asshole?)
•	countHeSheThey: How many times He/She/They is said in the body of the text. (Does number of times OP (original poster) mentions others correlate in either direction to being an asshole (being thoughtful, or placing blame on others)?
•	IvsHeSheThey: countI divided by countHeSheThey. Does any proportion between these two numbers suggest being/not being an asshole?
•	post_word_count: The length of the post.
•	questionmarklast: Whether or not the post ends in a question mark (does asking versus saying, in this case, the last sentence, suggest a humility or arrogance?).
•	WIBTA_AITA: Whether the title asks "Would I be the asshole", versus "Am I the asshole" -- are there any differences in decision based on choosing one or the other?
•	bodyreadinglevel: Estimating the reading level of the body text.

Objectives:

   - Perform an EDA on the data to develop an understanding of the dataset, the number of people determined to be assholes or not, and what features or characteristics best determine thar someone is or is not an asshole as judged by the community.
   - Use the EDA to determine the optimal features for modeling. 
   - Run models and compare between them to see which performs best (between XGBoost, Random Forest, Decision Tree, and Logistic Regression).
    

Reports

[Jupyter notebook for data cleaning](https://github.com/rjmalka/Capstone2_AITA/blob/master/notebooks/AITA_Clean_Final.ipynb)

[Jupyter notebook for Exploratory Data Analysis and Modeling](https://github.com/rjmalka/Capstone2_AITA/blob/master/notebooks/AITA_FINAL.ipynb)

[Capstone Project II Final Report](https://github.com/rjmalka/Capstone2_AITA/blob/master/report/AITA%20Report.pdf)

[Capstone Project II Final Presentation](https://github.com/rjmalka/Capstone2_AITA/blob/master/report/AITA_Capstone_Final_Slides.pdf)
