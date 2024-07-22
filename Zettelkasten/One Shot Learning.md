---
tags:
  - machine-learning
---
A concept used on [[Machine Learning]] where the problem is described in a way that the model must use one input only to recognised that thing.

As an example, a Face Recognition might have only one image from that person to now on being able to recognise that person in no matter how many other photos/videos.

*Deep learning obviously don't work well with that*

On way to "address" this type of problem is building a model that *instead predicting a class/number for those inputs* the model predicts the *difference between the new input (or the [[Similarity function|similarity]]) against each one that we have on the database*.