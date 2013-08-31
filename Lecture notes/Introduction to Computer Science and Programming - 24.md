# Introduction to Computer Science and Programming
## Lecture 24

### Statistical fallacies
For most of history, until the 17th century, quantitative analysis was unused. First use: when people died in London, to predict spread of the plague. Statistics can be used to inform or misinform.

#### In graphing
Statistics do not tell the whole story. By picking and choosing from a data set, any conclusion can be drawn. For example, multiple data sets with the same mean and linear regression; but once graphed, these look much different. Tip: Never ignore the data, look at the data itself. But be careful in how you graph, a graph can also be misleading. For example, a graph of housing prices in the midwest looks very stable or unstable depending on scale (linear vs. logarithmic) and range of Y axis, and the resolution of X axis (the intervals) changed from annually to seasonally.

#### Garbage in, garbage out (GIGO)
Some claim that measurement errors, while present, are unbiased and independent of one another, and therefore almost identically distributed on either side of the mean. These assumptions can be incorrect.

#### Cum Hoc Ergo Propter Hoc fallacy ("With this therefore because of this")
Correlation is not causation (e.g., students who attend lectures receive better grades, going to school causes the flu [flu peaks during school sessions]). The same (bad) logic could apply in reverse: the growth in flu causes people to go to school. One should attempt to identify a *lurking variable*, e.g., non-school season coincides with summer (flu virus survives in cold, dry environments).

Another example: hormone replacement therapy helps avoid cardiac disease; then a study published the opposite conclusion. How? Woman on hormone replacement therapy were more health conscious (better diet, exercise); these were the causative factors in better cardiac health. They (going on home replacement therapy and better cardiac health) were both *coincident effects*.

*Non-response bias* and *non-representative sample* problems: Usually samples provide the same distribution as the population as a whole, but the samples must be random. Often surveys rely on *convenience sampling*, a type of non-representative sample (e.g., professors using undergraduates as samples). Another example (non-response bias): In WWII, planes would return damaged and they'd use damage analysis to reinforce planes in the future (oops!). Telephone polls can't call mobile phones; their owners are undersampled.

#### Data enhancement
For example: CNN reported deaths and illnesses of swine flu (seemed high), but compared to seasonal flu (much, much higher), it's small. Or most traffic accidents occur within 10 miles of home (as does most driving!).

#### Extrapolation
*Extrapolation* can also be problematic (e.g., Internet usage in the U.S. appears to grow linearly).

#### Texas sharpshooter fallacy
The *Texas sharpshooter fallacy* is based on a a farmer shot six times at a barn, perfectly hit targets, but the farmer shot at the barn and *then* painted the targets. One study of 446 women suggested that anorexic women were born on certain months. On June, 48 of the anorexic women were born. How likely is that by chance? In a Python simulation, 4.2% probability of it occurring by chance (seems low). Scientists looked at data and changed hypothesis (June is more likely). Change simulation to calculate the probability of one month has 48 months: 42.5% (high!); therefore shouldn't draw any conclusion, the probability of it by pure chance is roughly half.