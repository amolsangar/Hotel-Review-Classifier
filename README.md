# Hotel-Review-Classifier

- The problem is to classify multiple hotel reviews in two categories – Deceptive and Truthful. To solve this problem, the use of naïve bayes makes perfect sense as we can select the category based on the probability of each word in the corpus and multiplying them. 
- The first step to perform is to clean the data into a list or dictionary of words excluding special characters and numbers and then converting to lowercase characters. Then, the task is to remove words which are quite common and doesn’t contribute much to the prediction of the classes. Examples of such stop words are if, an, the, that etc.
- After data cleaning and splitting into words, the program calculates prior probability and likelihood terms. Prior probability is calculated by dividing numbers of reviews in one class by number of reviews in every other class. Example – P(Deceptive) = P(Deceptive) / P(Deceptive) + P(Truthful)

- Next is to calculate likelihood term for each term i.e.,

  - P(Word | Deceptive) = Number of times Word occurs in review + alpha / Total number of words in Deceptive + alpha * Total number of words in the vocabulary

  Here, alpha is called as Laplace smoothing parameter and is used to handle the problem of zero probability.

- The last step is to calculate posterior probability which is simply multiplying likelihood and prior probability. Using log, we can do the same multiplication as - log(A*B) = logA + logB.

- Finally, the program cleans the input test reviews the same way as the training data and predicts the class output.

### Classification accuracy = 85.50%
