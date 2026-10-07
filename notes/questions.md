# Project Questions

These are the questions this project is built to answer. They guide which dbt marts I build, and later they become the test set for the chatbot: each question gets hand-written SQL and a known answer, and I check the chatbot's results against them.

| # | Question | Columns needed | Status |
|---|---|---|---|
| 1 | What are the top 10 highest-rated games with at least 1,000 ratings? | rating, number of ratings | Not started |
| 2 | What are the best games that support exactly 2 players? | min players, max players, rating | Not started |
| 3 | What are the best cooperative games under 90 minutes? | mechanics, play time, rating | Not started |
| 4 | What are the best solo-friendly games? | mechanics or min players | Not started |
| 5 | What are the best party games for 6 or more players? | domains or categories, max players | Not started |
| 6 | Which mechanics have the highest average rating? | mechanics, rating | Not started |
| 7 | Do heavier (more complex) games tend to rate higher? | complexity, rating | Not started |
| 8 | How has the number of games published changed by year? | year published | Not started |
| 9 | What are the best games for beginners? | complexity, play time, min age | Not started |
| 10 | Which games have data problems, like impossible player counts or missing years? | player counts, year | Not started |

## Stretch questions
- Euro vs. thematic games: how do they compare? (Approximate, using domains and complexity. There's no direct field for this.)

## Questions this data can't answer
Rules, where to play online, trivia, and storage. These need outside sources, not game data.

## Notes
- Column names will be updated to match the chosen dataset.
- Later, add a section per question with the hand-written SQL and the correct answer.
