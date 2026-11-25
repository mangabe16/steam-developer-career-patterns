| Attribute | Statistical Data Type | What it describes |
| :--- | :--- | :--- |
| AppID | Categorical, identifier | Unique identifier given to each game by Steam |
| Name | Categorical | Name of the game |
| Release date | Ordinal | Date when the game was released |
| Estimated owners | Ratio | Range scale formatted as a string of estimated count of owners for the game |
| Peak CCU | Ratio | Count of highest concurrent players playing the game at a given time |
| Required age | Ratio | Minimum age required to play the game in years |
| Price | Continuous | Cost in USD of the game on the Steam store |
| Discount | Ratio / Continuous | Discount offered at the time of scraping on the Steam store (percentage) |
| DLC count | Ratio | Count of how many DLC (downloadable content) available for the game |
| About the game | Text (Categorical) | Short blurb describing the game |
| Supported languages | Categorical | List of languages supported for the game |
| Full audio languages | Categorical | List of languages supported for the game for in-game audio |
| Reviews | Text (Categorical) | User reviews text or summary |
| Header image | Categorical (URL) | Link to an image displayed at the Steam store for the game |
| Website | Categorical (URL) | Link to the website for the game |
| Support url | Categorical (URL) | Link to the support page for the game |
| Support email | Categorical (URL) | Link to the support email for the game |
| Windows | Boolean (Categorical) | Whether there is Windows OS support for the game |
| Mac | Boolean (Categorical) | Whether there is Mac OS support for the game |
| Linux | Boolean (Categorical) | Whether there is Linux OS support for the game |
| Metacritic score | Interval / Ratio | Score metric by critics to the game, measured on a normalized 0 to 100 rating scale / points |
| Metacritic url | Categorical (URL) | Link to the critics page |
| User score | Interval / Ratio | Score given by users, typically measured on a 0 to 100 or 0 to 10 scale |
| Positive | Ratio | Count of how many “positive” votes were given to the game |
| Negative | Ratio | Count of how many “negative” votes were given to the game |
| Score rank | Ordinal / Ratio | Internal ranking based on the ratio between positive and negative reviews, measured as a percentile rank or ranking index |
| Achievements | Ratio | Total count of Steam achievements available to unlock the game |
| Recommendations | Ratio | Count of positive recommendations submitted by users |
| Notes | Text (Categorical) | Notes and warnings regarding the game |
| Average playtime forever | Ratio | Mean total playtime across all owners since the game’s release, measured in minutes |
| Average playtime two weeks | Ratio | Mean playtime per player in the 2 weeks preceding scraping, measured in minutes |
| Median playtime forever | Ratio | Median total playtime recorded across all owners since release, measured in minutes |
| Median playtime two weeks | Ratio | Median playtime recorded per player during the previous two-week period, measured in minutes |
| Developers | Categorical | Name of the developers |
| Publishers | Categorical | Name of the publishers |
| Categories | Categorical | Technical and platform capabilities provided by Steam |
| Genres | Categorical | High-level store genres assigned by the publisher/developer |
| Tags | Categorical | Community-applied descriptive tags reflecting gameplay themes, sub-genres, and tone |
| Screenshots | Categorical (URL) | Link to the screenshots available at the game page on Steam Store |
| Movies | Categorical (URL) | Link to the movies available at the game page on Steam Store |