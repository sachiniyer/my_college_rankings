# Ranking colleges

I am thinking about masters programs and wanted to find the programs that align with me the best.

https://csrankings.org is great, but I wanted to create a meta ranking based on all the factors that are important to me.
I also wanted to be able to assign custom weights to everything.

Data Source:

1. Conference Paper acceptances
2. Best Paper acceptances
3. Where professors did Bachelors/Masters

Very intentionally, no inclusion of citations

Stats:

1. Sum
2. Mean
3. Median
4. Max
5. Min
6. Variance
7. Standard Deviation

You create a meta ranking with the data sources and the stats you want. For example, I can put a large positive weight on mean conference paper acceptances and small negative weight on variance of conference paper acceptances. This might create the outcome of have a well distributed faculty where everyone publishes (with few laggards).

# Acknowledgements

## Data

This is the same as in the notebook.

[Data Archive Download Link](https://share.sachiniyer.com/share/FrbjszTR)

### CS Rankings Author info

Taken from https://github.com/emeryberger/CSrankings/tree/gh-pages which is the repo behind https://csrankings.org

Run `make generated-author-info.csv` which should make the csv. Each row contains the score for every author, year, and conference combination. This means that there are multiple rows for each professor.

### CS Professors

Taken from https://drafty.cs.brown.edu/csprofessors but they hide the data. So, after reading source code, exploit a [thing they left in](https://github.com/brownhci/drafty/blob/212bd995c857a34c74c7a71d67e1556c1ca7ea97/backend/src/controllers/datasharing.ts#L31) during development and use https://drafty.cs.brown.edu/data/csv/csprofessors/csprofessors_93318b344889ccef41d46b5f83d63de5

### Placement Rank

Taken from https://drafty.cs.brown.edu/csopenrankings/placement-rank.html which is just copy and paste (and `M-x query-replace <tab> ,`). I think I could have done this myself, but why do that when someone else has already done the work.

### Best Paper awards

A collection of best paper awards are listed on https://jeffhuang.com/best_paper_awards/

However, I needed to do some html parsing in order to get the data into a csv format. That is done in [another notebook](./best-paper.ipynb)

## Rankings Inspiration

They were good for inspiration when building mine

1. https://drafty.cs.brown.edu/csopenrankings/
2. https://drafty.cs.brown.edu/csprofessors
3. https://jeffhuang.com/best_paper_awards/institutions.html
4. https://drafty.cs.brown.edu/csopenrankings/placement-rank.html
5. https://airankings.org/
6. https://www.shanghairanking.com/rankings/gras/2022
