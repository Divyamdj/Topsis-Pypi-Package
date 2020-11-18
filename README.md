# TOPSIS-Python

**Assignment 6: UCS538**


Submitted By: **DIVYAM JAIN-101803128**

***

## What is TOPSIS

**T**echnique for **O**rder **P**reference by **S**imilarity to **I**deal
**S**olution (TOPSIS) originated in the 1980s as a multi-criteria decision
making method. TOPSIS chooses the alternative of shortest Euclidean distance
from the ideal solution, and greatest distance from the negative-ideal
solution. More details at [wikipedia](https://en.wikipedia.org/wiki/TOPSIS).

<br>

## How to use this package:

TOPSIS-Divyam-101803128 can be run as in the following example:



### Python Script
```
from topsis_101803128.topsis import CalcTopsisScore
filename = "input.csv"
weight = "1,1,1,2"
impact = "+,+,-,+"
CalcTopsisScore(filename, weight, impact )
```
<br>


## Sample dataset

The decision matrix (`a`) should be constructed with each row representing a Model alternative, and each column representing a criterion like Accuracy, R<sup>2</sup>, Root Mean Squared Error, Correlation, and many more.

Model | Correlation | R<sup>2</sup> | RMSE | Accuracy
------------ | ------------- | ------------ | ------------- | ------------
M1 |	0.79 | 0.62	| 1.25 | 60.89
M2 |  0.66 | 0.44	| 2.89 | 63.07
M3 |	0.56 | 0.31	| 1.57 | 62.87
M4 |	0.82 | 0.67	| 2.68 | 70.19
M5 |	0.75 | 0.56	| 1.3	 | 80.39

Weights (`w`) is not already normalised will be normalised later in the code.

Information of benefit positive(+) or negative(-) impact criteria should be provided in `I`.

<br>

## Output

Model | Correlation | R<sup>2</sup> | RMSE | Accuracy | Score | Rank
------------ | ------------- | ------------ | ------------- | ------------ | ------------ | ------------
M1 |	0.79 | 0.62	| 1.25 | 60.89 | 0.77221 | 2
M2 |  0.66 | 0.44	| 2.89 | 63.07 | 0.225599 | 5
M3 |	0.56 | 0.31	| 1.57 | 62.87 | 0.438897 | 4
M4 |	0.82 | 0.67	| 2.68 | 70.19 | 0.523878 | 3
M5 |	0.75 | 0.56	| 1.3	 | 80.39 | 0.811389 | 1


<br>
The rankings are displayed in the form of a table using a package 'tabulate', with the 1st rank offering us the best decision, and last rank offering the worst decision making, according to TOPSIS method.

## License

© 2020 Divyam Jain

This repository is licensed under the MIT license. See LICENSE for details.