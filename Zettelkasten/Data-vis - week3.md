---
tags:
  - data-vis
---

In this class they defined [[Graph]].

# Quantities data
## points
- minimal, visible mark
- data encoded by *location*
![[Pasted image 20240307175921.png|300]]

## lines
- emphasise trends
- has reference information
- data encoded by *position, shape and slope*
![[Pasted image 20240307180003.png|300]]

## bars as marks
- data encoded by *length*
- **better than points/lines for emphasising and comparing individual values**
- always scale from 0
![[Pasted image 20240307180209.png|300]]

## Pie chart
- Try to never use it! Bars are better: because *areas are difficult to compare not being adjacent or if difference is small* in pie charts.

## Bubble charts
- the problem with bubble chart is that *people tend to compare diameter rather than area* so the third variable (the one used to define the area) must be the *least important variable*
![[Pasted image 20240307180854.png|300]]

## Bullet graph
Useful to show a quantitative value in relation to some target or benchmark
![[Pasted image 20240307182528.png|500]]


# Categorical data

*Position is the most important feature*, followed by *hue as the second best choice*.
Prefer soft colours and good contrast.
![[Pasted image 20240307181040.png|300]]

# Relationships in graphs

Seven types of relationships can be visualised in graphs

## 1. Nominal Comparison
Comparing values between unordered groups. Bars are best choice.
![[Pasted image 20240307181319.png|200]]

## 2. Time series
goal is perceive trend/trajectory. Lines are good option.
![[Pasted image 20240307181452.png|200]]

## 3. Distribution
How are quantitative values distributed in a sample. Frequency histogram here!
![[Pasted image 20240307181724.png|200]]

If many categories, box plot!
![[Pasted image 20240307181812.png|200]]
[[Tukey's 5 number summary]]
## 4. Correlation
How two variables co-vary. Lines + regression. You can use enclosure to highlight outliers.
![[Pasted image 20240307181923.png|200]]

## 5. Ranking
Used to convey low-high(or high-low) relationship between categories.
Bars are good here and sort them accordingly!
![[Pasted image 20240307182120.png|200]]

## 6. Deviation
Shows the degree to which a quantitative variable differs.
Bars are good with a reference mark (two ways)
![[Pasted image 20240307182317.png|200]]

in combination with timeseries, lines is better
![[Pasted image 20240307182346.png|200]]

## 7. Part to whole
How some category is represented in a whole. Bar charts are the goal here, but you can go with stacked bars (tho, harder to compare)
![[Pasted image 20240307182737.png|200]]
![[Pasted image 20240307182752.png|200]]

# more than 3 dimensions - Multi-D

Usually we use Machine learning (clustering and dimensionality reduction).

E

