# Stance-Detection-and-Rumour-Verification

<p>
Rumors are rife on the web. False claims affect people’s perceptions of events and their behavior, sometimes in harmful ways. With the increasing reliance on the Web – social media, in particular – as a source of information and news updates by individuals, news professionals, and automated systems, the potential disruptive impact of rumors is further accentuated.
Within NLP research the tasks of (i) stance classification of reddit posts and social media posts and (ii) the creation of systems to automatically identify false content are gaining momentum. The project requires completing two of the RumourEval 2019 tasks, the first task is to classify/ detect stances of a tweet’s reply thread and the second task is to verify the rumor introduced by the source tweet credibility. In addition to that, a task of generating stance text given a source tweet, prior tweets in the conversation thread and a stance classification label is introduced.

Dataset: The data are structured as follows. Source posts introduce a rumor and may be true, false or unverified. These are accompanied by an ensuing discussion (tree-shaped) in which users support, deny, comment or query (SDCQ) the rumor in the source text.
Dataset link: https://figshare.com/articles/dataset/RumourEval_2019_data/8845580

<strong>Task Definitions</strong>:

● Subtask A - SDQC support classification: given a source tweet, tweets in a conversation thread discussing the claim are classified as either supporting, denying, querying or commenting on the rumor mentioned by the source tweet. Success on this task supports success on task B by providing additional context and information; for example, where the discussion ends in a number of agreements, it could be inferred that human respondents have verified the rumor.

● Subtask B - Veracity prediction: the goal of subtask B is to predict the veracity of a given rumor. The rumor introduced by the source tweet that spawned the discussion is classified as true, false or unverified. Use of additional information from context and Subtask A results can significantly improve the performance. In addition to returning a classification of true, or false, a confidence score was also required, allowing for a finer-grained evaluation. A confidence score of 0 should be returned if the rumor is unverified.

● Subtask C - Stance Generation: the goal of this task is to train a language model to generate a stance text(R) given a source tweet(S), tweets in a conversation thread discussing the claim (CTX) and the stance prediction label (L) from Subtask A, where the conditional distribution of the stance text(R) is p(R|S,CTX,L). The model should be trained by minimizing the language modeling loss between the generated stance text(R) and the golden stance text Y.

<strong>Evaluation Metrics</strong>:

● Subtask A: Macro-averaged F1 is used to evaluate the classification performance.

● Subtask B: Again, macro-averaged F1 is used to evaluate the classification performance. For the confidence score, a root mean squared error (RMSE, a popular metric that differs only from the Brier score in being its square root) is to be calculated relative to reference
confidence of 1.

● Subtask C: The following metrics should be calculated between the generated text in the
test set and the golden response. Each metric should be compared against suitable external and internal baselines:

● Perplexity (https://en.wikipedia.org/wiki/Perplexity)

● BLEU score (https://en.wikipedia.org/wiki/BLEU)

● ROUGE score (https://en.wikipedia.org/wiki/ROUGE_(metric))

● BERT Score (https://github.com/Tiiiger/bert_score)

● BLEURT Score (https://github.com/google-research/bleurt)

<strong>References</strong>: RumourEval 2019 summary paper: https://www.aclweb.org/anthology/S19-2147.pdf
</p>
