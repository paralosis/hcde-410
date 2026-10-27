Exercises and assignments for HCDE410: Human Data Interaction. Everything here is a work in progress unless otherwise noted :)

#HCDE410
Files for HCDE410 - Assignment A2

**Dataset:** Wikipedia Talk Labels
**Sources:** https://figshare.com/projects/Wikipedia_Talk/16731
             https://github.com/brockcraft/hcde410/blob/main/A2/toxicity_labelled_comments_3k_sample.csv
**License / terms of use:** https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt

## Questions I asked & response
**1. What is the gender distribution of these workers?**
The gender distribution is 63.59% male, 36.38% female, and 0.03% other.

**2. What is the distribution of the workers by first language?**
Workers with English as not their first language is 81.53%, while workers with English as their first langugage is 18.47%.

**3. What is the distribution of these workers by age group?**
The age group with the highest percentage of workers is 18-30 with 51.35%, 30-45 at 36.66%, 45-60 at 9.07%, under 18 at 2.05%, and over 60 with the lowest at 0.88%.

**4. what is the distribution of these workers by education level?**
The distribution of workers for education level goes from bachelors (39.84%), high school (28.66%), masters (16.10%), professional (11.83%), some (2.44%), docotorate (1.06%), and none (0.07%).

**5. Analyze all_annotators in Sheets or Jupyter: Do any of the fields in this dataset have missing data? If so, which fields, and what % of the rows contain missing values?**
I noticed missing fields in the dataset for age_group, where 1.94% of the rows contained missing values.

**6. Build a version of the all_annotators dataset *without removing duplicates*, then re-run the summary statistics from questions 1-4. How have these summary statistics changed?**
The summary statistics for the all_annotators dataset with duplicates has a higher count compared to the original all_annotators without duplicates. The percentages have a slight difference between the datasets, which could be because of the difference in the counts. In the age_group summary statistics, the all_annotators with duplicates has an additional row for the missing fields, which isn't present in the all_annotators without duplicates.

**7. In general, how do the demographics of these workers compare to those of English-speaking internet users overall? Why would it matter if the worker demographics don't match the demographics of the intended end users of the Perspective API?**
There are more English-speaking internet users (25.9% from this [source](https://www.quantumrun.com/consulting/english-language/)) than the worker demographic (around 18.44%). I think that there would disconnect between the users and workers, especially when a higher percentage of workers don't have English as their first language. There could be misunderstandings and errors when marking commentary made by users. 

**8. Given what you now know about the Wikipedia Talk Corpus, what issues might arise if it was used to train a machine learning-driven "hostile speech detector" that could be used on any website or social media platform?**
Issues could arise when it flags the wrong comments as hostile speech, or if it doesn't detect a comment as hate speech. In the previous question, we can see that there can be a disconnect in language between the users and workers, which could lead to issues when an automated system is flagging the comments based on the Wikipedia Talk Corpus.

**9. Pick 2-3 examples of comments where you disagreed with the labeller about the toxicity of a comment. Why did you disagree? Why do you think that the labeller might have labelled these comments the way they did?**
Two comments that I found were labelled as "toxic" (-1):
1. NEWLINE_TOKENNEWLINE_TOKEN== Doogle ==NEWLINE_TOKENNEWLINE_TOKENWell done! How on earth did you manage to assess Doogle for notability in two minutes flat? Here's a friendly suggestion - don't just immediately delete things - have a quick word with the author first, especially if he's an established editor. I'm going to re-instate the article. Thanks.

2. NEWLINE_TOKEN::: Take it to the talk no sense having discussion in 2 places.

I disagreed with these comments because they don't have any apparent toxic comments or words used, but there could be lacking context in the entire conversation that could deem this comment as toxic, but I'm only basing my judgement on the provided comment. The labeller could've had the context for the comment that could've influenced their judgement, or they could've judged the underlying tone of the comment, which also depends on who the labeller is and their tolerance for toxicity.

**10. Pick 2-3 examples of comments where you don't understand what the commenter was saying, and therefore had a hard time classifying as toxic or non-toxic. What additional context or information would you need in order to be confident in your judgement about the toxicity of this comment?**
1. NEWLINE_TOKEN::::::If by sleuthing you mean trying to enhance my understanding of policy, I don't appreciate your terminology. You actually protected it for two weeks. You shortened it after I was unblocked by Protego and had numerous times expressed my concern with your excessive use of tools, correct? I don't really care if you read these anymore, but if someone else does my responses are present.

2. NEWLINE_TOKENNEWLINE_TOKENNEWLINE_TOKEN99.99% sureNEWLINE_TOKENNEWLINE_TOKENWhen it comes to the military 8k DEADNEWLINE_TOKENNEWLINE_TOKENThe rest were either sent to work camps or prisons.NEWLINE_TOKENNEWLINE_TOKEN( )

The first comment was labelled neutral (0) but it was a little confusing on what the user is discussing. It would need context on the discussion and what they are responding to, which could help determine the underlying tone of this comment.
it was confusing on what the commenter is responding to and the tone of their exchange with another user. 
The second comment was labelled toxic (-1) but it would also need context for where the discussion took place, the overall context of the discussion, and any follow-up comments made by the same user. At a glance, this comments seems to be labelled as toxic because of key words used in the comment, but it's hard to make a judgement whether they were being toxic or informative.

**11. Read through the [instructions and labelling options](https://github.com/ewulczyn/wiki-detox/blob/master/src/modeling/toxicity_question.png) given to the crowdworkers. How could the way these instructions were written have made it difficult for crowdworkers to accurately label comments as toxic or non-toxic? If you were going to run a labelling campaign like this one yourself, how would you change these instructions or labelling options to help the crowdworkers make more accurate or consistent judgements about toxicity?**
One thing that stands out to me is that all labels have a short description except for neither, which could make it a default choice if the labeller is unsure if a comment goes into 1 or -1. The descriptions themselves seem a little vague, especially between toxic and very toxic, and I feel like it would be harder for the crowdworkers to distinguish between these two. It would be helpful to implement a list of categories the comments would fall under, similar to user guidelines for social media platforms such as the use of hate speech, violence, misinformation, etc. It would also be helpful for comments labelled toxic (-1 and -2) to be reviewed by more than one person, which could help with determining how toxic a comment is.

**12. Based on your findings from questions 13-15, how might this dataset present a biased view of "toxicity"? How would you expect such biases to impact how the Perspective API performs as a general-purpose hostile speech detector?**
Based on your findings from questions 13-15, how might this dataset present a biased view of "toxicity"? How would you expect such biases to impact how the Perspective API performs as a general-purpose hostile speech detector? 

My findings were mostly about the lack of context for comments and the discussions they take place in, as well as crowdworkers having vague descriptions for labelling comments and their judgement on a comment based on their own interpretations, which could lead to some comments being mislabeled or too confusing to label at a glance. This could present information, demographic, and confirmation bias for this dataset and how it views toxicity. Another point I would like to make is the culture of a platform, such as Wikipedia, has it's own norms and speech that could be different from another platform. So the "toxicity" in this dataset would only apply to the Wikipedia Talk Pages, since toxicity would look a lot different on Tiktok or Youtube.

I would expect these biases to show up in a speech detector when it analyzes a comment for a pattern of speech or keywords that was flagged as toxic in this dataset, and then automatically label that comment as toxic or non-toxic without human intervention to understand human speech/text. 

## How to re-run
Download 'toxicity_labelled_comments_3k_sample.csv' from the Github and 'wikipedia_datasets' from the Github or Figshare, this contains the 'aggression_worker_demographics.tsv', 'attack_worker_demographics.tsv', and 'toxicity_worker_demographics.tsv'.

Open `A1.ipynb` and run all cells (needs `requests`, `pandas`, `matplotlib`).
