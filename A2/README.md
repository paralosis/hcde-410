Exercises and assignments for HCDE410: Human Data Interaction. Everything here is a work in progress unless otherwise noted :)

#HCDE410
Files for HCDE410 - Assignment A2

**Dataset:** Wikipedia Talk Labels
**Source:** https://figshare.com/projects/Wikipedia_Talk/16731
**License / terms of use:** https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt

## Questions I asked & response
**1. What is the gender distribution of these workers?**
The gender distribution is 63.59% male, 36.38% female, and 0.03% other.

**2. What is the distribution of the workers by first language?**
The age group with the highest percentage of workers is 18-30 with 51.35%, 30-45 at 36.66%, 45-60 at 9.07%, under 18 at 2.05%, and over 60 with the lowest at 0.88%.

**3. What is the distribution of these workers by age group?**

**4. what is the distribution of these workers by education level?**

**5. Analyze all_annotators in Sheets or Jupyter: Do any of the fields in this dataset have missing data? If so, which fields, and what % of the rows contain missing values?**

8. Build a version of the all_annotators dataset *without removing duplicates*, then re-run the summary statistics from questions 1-4. How have these summary statistics changed?

9. In general, how do the demographics of these workers compare to those of English-speaking internet users overall? Why would it matter if the worker demographics don't match the demographics of the intended end users of the Perspective API?

10. Given what you now know about the Wikipedia Talk Corpus, what issues might arise if it was used to train a machine learning-driven "hostile speech detector" that could be used on any website or social media platform?

11. Pick 2-3 examples of comments where you disagreed with the labeller about the toxicity of a comment. Why did you disagree? Why do you think that the labeller might have labelled these comments the way they did?

12. Pick 2-3 examples of comments where you don't understand what the commenter was saying, and therefore had a hard time classifying as toxic or non-toxic. What additional context or information would you need in order to be confident in your judgement about the toxicity of this comment?

13. Read through the [instructions and labelling options](https://github.com/ewulczyn/wiki-detox/blob/master/src/modeling/toxicity_question.png) given to the crowdworkers. How could the way these instructions were written have made it difficult for crowdworkers to accurately label comments as toxic or non-toxic? If you were going to run a labelling campaign like this one yourself, how would you change these instructions or labelling options to help the crowdworkers make more accurate or consistent judgements about toxicity?

14. Based on your findings from questions 13-15, how might this dataset present a biased view of "toxicity"? How would you expect such biases to impact how the Perspective API performs as a general-purpose hostile speech detector? 

## How to re-run
Open `A1.ipynb` and run all cells (needs `requests`, `pandas`, `matplotlib`).
