# Project Questions

These are the questions this project is built to answer. They guide which dbt marts I build, and later they become the test set for the chatbot: each question gets hand-written SQL and a known answer, and I check the chatbot's results against them.

Dataset: `ratings.csv` and `details.csv`, joined on `id`.

| # | Question | Columns needed | Status |
|---|---|---|---|
| 1 | What are the top 10 highest-rated games with at least 1,000 ratings? | `average`, `bayes_average`, `users_rated` | Not started |
| 2 | What are the best games that support exactly 2 players? | `minplayers`, `maxplayers`, `average` | Not started |
| 3 | What are the best cooperative games under 90 minutes? | `boardgamemechanic`, `playingtime`, `average` | Not started |
| 4 | What are the best solo-friendly games? | `minplayers`, `boardgamemechanic` | Not started |
| 5 | What are the best party games for 6 or more players? | `boardgamecategory`, `maxplayers`, `average` | Not started |
| 6 | Which mechanics have the highest average rating? | `boardgamemechanic`, `average` | Not started |
| 7 | Which games are most wished for compared to how many people own them? | `wishing`, `owned` | Not started |
| 8 | How has the number of games published changed by year? | `yearpublished` | Not started |
| 9 | What are the best games for beginners (short play time, low minimum age)? | `playingtime`, `minage`, `average` | Not started |
| 10 | Which games have data problems, like impossible player counts or missing years? | `minplayers`, `maxplayers`, `yearpublished`, `id` | Not started |

## Stretch questions
- Euro vs. thematic games: how do they compare? (Approximate, using categories. There's no direct field for this.)
- Which designers have the best track record? (`boardgamedesigner`, `average`)

## Questions this data can't answer
- Complexity vs. rating: this dataset has no complexity column.
- Rules, where to play online, trivia, and storage. These need outside sources, not game data.

## First findings from exploring the data
- `ratings.csv` has 21,831 games; `details.csv` has 21,631. 200 rated games have no details.
- List columns (mechanics, categories, designers) are stored as text that looks like a Python list. Some values contain commas inside the name (e.g. `'Deck, Bag, and Pool Building'`), so splitting on commas would break them.
- `name` vs. `primary` and `year` vs. `yearpublished` look like duplicates. Check whether they ever disagree.

## Notes
- Later, add a section per question with the hand-written SQL and the correct answer.