# Tweet Interaction Analysis — Power BI Project

A Power BI dashboard built to analyze tweet-level engagement data across six focused tasks — from simple engagement comparisons to time-gated, multi-condition breakdowns. The project uses a single tweet-activity dataset (Tweet.xlsx) and explores how different interaction types (clicks, replies, retweets, likes, media views) behave under various filtering rules.

## Dataset Overview
`Tweet.xlsx` contains one row per tweet, with columns for:

- **Tweet text and ID**
- **Timestamp**
- **Impressions and engagements** (and engagement rate)
- **Retweets, replies, likes**
- **Click-type interactions:** URL clicks, hashtag clicks, user profile clicks, detail expands, permalink clicks
- **App-related actions:** app opens, app installs, follows, email tweet, dial phone
- **Media metrics:** Media views and media engagements

## Tools Used
- **Power BI Desktop:** Used for data modeling, creating DAX measures, and designing report visuals.
- **Power Query:** Used for data shaping and generating derived columns (such as even/odd date flags and character/word counts).
- **Excel:** Source dataset formatting.


## Project Tasks & Business Logic

To demonstrate advanced data shaping and DAX capabilities, this dashboard was built to satisfy six highly specific, complex business requirements:

**1. Tweet Interaction Breakdown by Category**
- **The Goal:** Analyze how different tweet types drive user interactions using a clustered bar chart to compare URL, user profile, and hashtag clicks.
- **Complex Logic Applied:** The visual is dynamically time-gated to only appear between 3 PM and 5 PM IST. The data is strictly filtered to only include tweets with an even-numbered date and a word count greater than 40.

**2. Engagement Rate Comparison (App Opens)**
- **The Goal:** Evaluate how app interactions influence overall engagement by comparing tweets with and without app opens.
- **Complex Logic Applied:** Applied strict weekday scheduling (9 AM - 5 PM). Time-gated visual visibility to 12 PM - 6 PM IST and 7 AM - 11 AM IST. Built custom filters to only include even-numbered impressions, odd-numbered dates, character counts > 30, and specifically excluded any tweets containing the letter ‘D’.

**3. Media Interaction by Day of Week**
- **The Goal:** Identify patterns in media engagement across the week using a dual-axis chart to track media views and engagements over the last quarter.
- **Complex Logic Applied:** Visual visibility restricted to 3 PM - 5 PM IST and 7 AM - 11 AM IST. Filtered for even impressions, odd dates, >30 characters, and excluded text containing the letter ‘H’.

**4. Replies, Retweets, and Likes Comparison**
- **The Goal:** Understand core engagement metrics using a bar chart comparing total replies, retweets, and likes using SUM aggregations.
- **Complex Logic Applied:** Applied targeted date-range filtering to isolate data specifically between June and August 2020.

**5. Monthly Engagement Rate Trend**
- **The Goal:** Track engagement trends over time by month.
- **Complex Logic Applied:** Segmented the data dynamically into two comparative line charts to pit tweets with media content against those without.

**6. Top 10 Tweets by Engagement**
- **The Goal:** Identify high-performing tweets and their creators based on total retweets and likes.
- **Complex Logic Applied:** Excluded weekend data. Time-gated the chart to only display between 3 PM and 5 PM IST. Filtered specifically for concise tweets (word count < 30) that occurred on odd dates with even impressions.
