---
tags:
  - machine-learning
---
*7 steps of Machine Learning*:
1. Gathering Data
2. Preparing that data
3. Choosing a Model
4. Training
5. Evaluation
6. Hyperparameter Tuning
7. Prediction

---

**Problem framing** is the process of analyzing a problem to isolate the individual elements that need to be addressed to solve it.

To understand the problem, perform the following tasks:
- State the goal for the product you are developing or refactoring.
- Determine whether the goal is best solved using predictive ML, generative AI, or a non-ML solution.
- Verify you have the data required to train a model if you're using a predictive ML approach.

ML systems can be divided into two broad categories: [**predictive ML**](https://developers.google.com/machine-learning/glossary#predictive-ml) and [**generative AI**](https://developers.google.com/machine-learning/glossary#generative-ai). The following table lists their defining characteristics:

![[Pasted image 20250316214444.png]]

To confirm that ML is the right approach, first verify that your current non-ML solution is optimized. If you don't have a non-ML solution implemented, try solving the problem manually using a [**heuristic**](https://developers.google.com/machine-learning/glossary#heuristic).

---

To make good [**predictions**](https://developers.google.com/machine-learning/glossary#prediction), you need data that contains [**features**](https://developers.google.com/machine-learning/glossary#feature) with predictive power. Your data should have the following characteristics:

- **Abundant**. The more relevant and useful examples in your dataset, the better your model will be
    
- **Consistent and reliable**. Having data that's consistently and reliably collected will produce a better model. For example, an ML-based weather model will benefit from data gathered over many years from the same reliable instruments.
    
- **Trusted**. Understand where your data will come from. Will the data be from trusted sources you control, like logs from your product, or will it be from sources you don't have much insight into, like the output from another ML system?
    
- **Available**. Make sure all inputs are available at prediction time in the correct format. If it will be difficult to obtain certain feature values at prediction time, omit those features from your datasets.
    
- **Correct**. In large datasets, it's inevitable that some [**labels**](https://developers.google.com/machine-learning/glossary#label) will have incorrect values, but if more than a small percentage of labels are incorrect, the model will produce poor predictions.
    
- **Representative**. The datasets should be as representative of the real world as possible. In other words, the datasets should accurately reflect the events, user behaviors, and/or the phenomena of the real world being modeled. Training on unrepresentative datasets can cause poor performance when the model is asked to make real-world predictions.

For a model to make good predictions, the *features in your dataset should have predictive power*. **The more correlated a feature is with a label, the more likely it is to predict it**.

---

You frame a problem in ML terms by completing the following tasks:

- Define the ideal outcome and the model's goal.
- Identify the model's output.
- Define success metrics.

![[Pasted image 20250316215822.png]] "Hiding your app's behavior from the model can cause your app to produce the wrong behavior."

---
 in the video app, the ideal outcome is to recommend useful videos. However, there's no label in the dataset called `useful_to_user.`

|**Ideal outcome**|**Ideal label**|
|---|---|
|_Recommend useful videos._|`?`|

Therefore, you must find a proxy label.

### Proxy labels

[**Proxy labels**](https://developers.google.com/machine-learning/glossary#proxy-labels) substitute for labels that aren't in the dataset. Proxy labels are necessary when you can't directly measure what you want to predict. In the video app, we can't directly measure whether or not a user will find a video useful. It would be great if the dataset had a `useful` feature, and users marked all the videos that they found useful, but because the dataset doesn't, we'll need a proxy label that substitutes for usefulness.

A proxy label for usefulness might be whether or not the user will share or like the video.

|**Ideal outcome**|**Proxy label**|
|---|---|
|_Recommend useful videos._|`shared OR liked`|

Be cautious with proxy labels because they don't directly measure what you want to predict. For example, the following table outlines issues with potential proxy labels for _Recommend useful videos_:

|**Proxy label**|**Issue**|
|---|---|
|Predict whether the user will click the "like" button.|Most users never click "like."|
|Predict whether a video will be popular.|Not personalized. Some users might not like popular videos.|
|Predict whether the user will share the video.|Some users don't share videos. Sometimes, people share videos because they **don't** like them.|
|Predict whether the user will click play.|Maximizes clickbait.|
|Predict how long they watch the video.|Favors long videos differentially over short videos.|
|Predict how many times the user will rewatch the video.|Favors "rewatchable" videos over video genres that aren't rewatchable.|

No proxy label can be a perfect substitute for your ideal outcome. All will have potential problems. Pick the one that has the least problems for your use case.