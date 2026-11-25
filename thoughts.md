## Our core question:
- Does releasing more games make a developer more succesful?

### Secondary questions
- Look at developer success according to release interval
- Look at developer success according to front page effort
- Are there natural groups of developer "types"?
    - One hit wonder
    - One hit flop
    - Many hit wonder
    - Many hit flop
    - Maybe more?
- Does the removal of adult games weaken our hypothesis?
    - What type of growth can be found? Linear, or a different kind?

## Mining methods
- A priori
    - Need to determine a meaningful threshold
    - Example question
        - Given 5 (or more) games produced, is there success?
            Need to establish a metric of success, add a column with a boolean of 'successful' or not
            Interested in looking at genre tags
- Clustering
    - Introduce more dimensions
    - Once meaningful clusters are found, we name them and call it a day
- Linear regression
    - Need to interpret the results a bit better

## Tasks

### Needed
- Clean, document, and finish the main notebook
- Add Jacob's graphs showing early signs of higher engagement as game_count increased to EDA section
- Write the final report

### In Progress
- Apply k-means on final, cleaned dataset
- Identify outliers

### Done
- Remove entries with missing developer field
- Transforms entries with at least 1 DLC into multiple rows
- Sensitivity analysis
- Apply regression
- Apply a priori



## Things to document
- Difficult to differentiate indie developers from AAA
- Why avg_price and game_count were capped
- The DLC count into extra game transformation

## Thoughts


Interesting questions to look for
    - Ascertain if there are "types"/clusters of developers        

- We are likely to have several datasets at the end of our process
    - Can compare subdatasets and look at correlations
    - Can recover sale information from proxies
    - Compare different metrics of success with their correlation to a game's success 
        
## Papers to look at
- David Arthur and Sergei Vassilvitskii. SODA, 2007, pp. 1027-1035.
    - https://research.google/pubs/k-means-the-advantages-of-careful-seeding/
    - K-Means++
        - Notes:
            - Introduces kmeans++, doesn't much help us in our project. Core focus is explaning the improvement kmeans++ brings and proves it
- Martin Ester, Hans-Peter Kriegel, Jorg Sander, and Xiaowei Xu. KDD, 1996.
    - https://file.biolab.si/papers/1996-DBSCAN-KDD.pdf
    - DBSCAN/Density-Based Clustering
        - Useful when clusters are non-spherical, when the number of clusters is not known in advance, or when noise points are important