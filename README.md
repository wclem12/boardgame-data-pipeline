# Board Game Data Pipeline

A learning project where I build a small end-to-end data pipeline on board game data, using the modern data stack: Snowflake, dbt, Git, and Python. I'm a Qlik developer with 9+ years of experience, and this project is how I'm adding these tools to my skills.

**Status:** In progress. This README will be updated as each piece is finished.

## Goals
- Load real data into a cloud warehouse (Snowflake)
- Clean and model it with dbt, including tests and documentation
- Use Python and pandas to profile and prep the raw files
- Build a small chatbot that answers board game questions in plain English by writing SQL against the finished tables
- Keep everything version controlled in Git

## Data
BoardGameGeek data from this Kaggle dataset:
[Board Games Database from BoardGameGeek](https://www.kaggle.com/datasets/threnjen/board-games-database-from-boardgamegeek)

The data is a snapshot from around 2021 to early 2022, so recent games are not included. The raw files are not stored in this repo. Download them from Kaggle to run the project.

## Planned architecture
1. **Raw files** from Kaggle
2. **Python and pandas:** profile the data and do light prep
3. **Snowflake:** load the raw tables
4. **dbt:** staging models, then intermediate models, then marts (final tables for analysis), with tests and docs
5. **Chatbot:** Claude turns a plain-English question into SQL, the app runs it against the marts, and Claude explains the result

## Tools
| Tool | Used for |
|---|---|
| Snowflake | Cloud data warehouse |
| dbt | Transforming, testing, and documenting the data |
| Python and pandas | Data profiling, prep, and the chatbot |
| Claude API | Natural-language questions over the data |
| Git and GitHub | Version control |

## Planned chatbot safeguards
- Read-only database role that can only see the final tables
- Only a single SELECT statement is allowed, with a row limit
- Limited number of questions per session
- A set of test questions with known answers to check the results

## Progress
- [ ] Explore the dataset with pandas
- [ ] Complete dbt Fundamentals course
- [ ] Load data into Snowflake
- [ ] Build dbt staging models
- [ ] Build dbt marts with tests and documentation
- [ ] Build the chatbot
- [ ] Test the chatbot against known answers

## Author
Will. See my [GitHub profile](https://github.com/your-username) for more about me.
