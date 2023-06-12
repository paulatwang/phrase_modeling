# Project Goals
The goal of this project was to create a step-by-step notebook to practice topic modeling using phrases (i.e., words clustered as bigrams and trigrams) instead of individual words as the unit of study. The initial question I tried to answer was: How do news topics differ between articles that use differentially moral language (e.g., care/harm language vs authority/subversion language).

## Theoretical Background
Moral Foundations Theory (MFT; Haidt & Joseph, 2007) assumes that there exists a set of innate and universally held moral intuitions that can be categorized into 5 general moral foundations: care/harm, fairness/cheating, loyalty/betrayal, authority/subversion, and sanctity/degradation. For each foundation, whether morality has been upheld or violated exists on a spectrum, the ends of which are denoted by the presence of a positively valenced signifier (e.g., care) or negatively valenced signifier (e.g., harm). The care/harm foundation refers to the innate desire to help those in need and mitigate harm; the fairness/cheating foundation refers to the drive to see people being treated with equality and equity; the loyalty/betrayal foundation refers to ingroup loyalty, which is a bias that favors benefits towards members of one’s ingroup members and against one’s outgroup members; authority/subversion foundation refers to the desire to follow a leadership figure and obey traditions and hierarchy; and finally, the sanctity/degradation foundation refers to the urge to pursue both tangible and abstractive cleanliness and purity, while rejecting spiritual and physical contamination.

## Data
- Text from 1m+ news articles computationally extracted from GDELT (Global Database of Events, Language, and Tone; Leetaru & Schrodt, 2013)

## Process
1. Separate articles by the moral foundation they correspond most closely to
2. Biuild corpus from each set of data: preprocess data, build bigrams/trigrams, create dictionary using bag-of-words approach, create corpus as set of dictionary-defined vectors, each representing a document within the dataset. 
5. Build models
6. Analyze models 

## Results
While the pipeline works smoothly, ultimately the major issue that I ran into (that I should have pre-empted), was that the articles cannot be cleanly divided into separate foundation categories. This is because while the separate foundations are conceptually distinct, they are not mutually exclusive. This allows any particular situation to be morally represented as a function of five dimensions that are based on the five foundations of morality. So there was therefore so much overlap between articles across the foundations, that the final topics generated were not conceptually distinct. 
