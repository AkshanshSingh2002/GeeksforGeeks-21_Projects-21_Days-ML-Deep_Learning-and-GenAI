## Day 2: Netflix Content Strategy Analysis

### Project Overview
This project performs an in-depth exploratory data analysis (EDA) of Netflix's content library to understand trends in content production, popular genres, ratings, and geographical distribution.

### Objectives
- Analyze content distribution (Movies vs. TV Shows)
- Identify temporal trends in content additions
- Explore genre popularity and geographical sourcing
- Examine content maturity ratings and duration patterns
- Engineer features for deeper insights (content age, freshness)

### Key Findings
- **70% of Netflix content is movies**, with accelerated growth 2016-2019
- **US is the largest producer**, followed by India, UK, and South Korea
- **TV-MA and TV-14 ratings dominate**, reflecting mature audience targeting
- **Most TV shows last only 1 season**, indicating high-risk original programming
- **Content themes revolve around relationships**: family, love, discovery

### Techniques Applied
- Data cleaning and type conversion (`pd.to_datetime`)
- Handling multi-value columns (genres, cast, directors via `.explode()`)
- Time-series analysis
- Feature engineering (content age, years to add)
- Word cloud generation for thematic analysis

### Submission Questions Answered
1. Content rating distribution over time
2. Relationship between content age and type
3. Release year vs. addition year trends
4. Common phrases in descriptions
5. Top directors on Netflix

### Files Included
- `2_Cracking_the_Code_An_Inside_Look_at_Netflix's_Content_Strategy.ipynb` - Main EDA notebook
- `L2_Assignment.ipynb` - Assignment solutions with visualizations

---
