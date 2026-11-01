## Our core question:
    - Does releasing more games make a developer more succesful?

    - Secondary questions
        - Look at developer success according to release interval
        - Look at developer success according to front page effort
        - Are there natural groups of developer "types"?
                - One hit wonder
                - One hit flop
                - Many hit wonder
                - Many hit flop
                - Maybe more?
            - Could aid in investment decision
                - Do I want to put my money in someone who is consistent?
        
        - Does the removal of adult games weaken our hypothesis?
            - What type of growth can be found? Linear, or a different kind?

## Tasks
- Clean data from unwanted columns: done
- Clean data from duplicates: done
- Clean data from missing entries
- Transforms entries with at least 1 DLC into multiple rows
- Apply k-means on final, cleaned dataset

## Plan of action for the weekend
- Clean the dataset
    - Remove duplicates
    - Drop columns we will not utilize
        -Need to define this!
    - Decide cleaning for N.A (should we just drop them? apply median? and for all columns, or just some)
    - Have a finished, cleaned, dataset, from which we begin mining
    - Apply k-means clustering
        - Do for different values for k

## Thoughts

- keep developers with 1 game published
- need to clean and aggregate the data
    - if one game has 2 developers, make duplicate that row
    - drop unused columns
- Could consider using K-means to evaluate quality of clusters
    - Iterate through number of clusters and evaluate their strength
        - SSE:Total within-cluster squared error
        - Elbow method: SSE always falls as K grows; look for diminishing returns.
- Looking for r -> the strength of correlation
    - number of games released x number of reviews
    - can do by genre
    make sure to have correlation line in the plot
    r value starts at 0
    pearson correlation matrix
    once r is found, you can state what kind of correlation was found
    in the distributiion, could ask if it is statistically significant
    looking at p-value

Interesting questions to look for
    - Ascertain if there are "types"/clusters of developers
        
    

- We are likely to have several datasets at the end of our process
    - Can compare subdatasets and look at correlations
    - Can recover sale information from proxies
    - Compare different metrics of success with their correlation to a game's success 
        

## Data Quality
- Need to finish table at `Looking at the shape and attributes of our data` section
    - Are dates ordinal? Categorical?
    - Are names also identifiers? or just AppID?
    - Is `Estimated Owners` ratio or discrete?


## Ideas for later
- consider using pd.cut() for binning values
    - we could have a new label for a developer/game, with the label low/high engagement

## For cleaning
- Standardize null representations: CSVs often use 'N/A', '-', 'null', or empty strings inconsistently. Pass na_values to read_csv or use replace() post-load to unify them before calling isna().
- Convert to appropriate types: Object columns containing repeated strings should become categories. Numeric columns stored as strings need pd.to_numeric(errors='coerce') to safely handle non-numeric garbage.
- Handle duplicates explicitly: Use duplicated(subset=[...], keep=False) to flag all duplicate records, not just subsequent ones, allowing manual review before dropping.
- Validate ranges and constraints: Apply business rules early. Negative amounts, future timestamps, or invalid status codes should be isolated into a separate error DataFrame rather than mixed into clean data.

## For aggregationa nd transformation
- look into `groupby()` and `transform()`