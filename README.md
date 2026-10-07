# Board Game Data Pipeline

A learning project where I build a small end-to-end data pipeline on board game data, using the modern data stack: Snowflake, dbt, Git, and Python. I'm a Qlik developer with 9+ years of experience, and this project is how I'm adding these tools to my skills. I'm also learning to work with an AI coding assistant (Claude Code) along the way.

**Status:** In progress. This README will be updated as each piece is finished.

## Goals
- Load real data into a cloud warehouse (Snowflake)
- Clean and model it with dbt, including tests and documentation
- Use Python and pandas to profile and prep the raw files
- Build a small chatbot that answers board game questions in plain English by writing SQL against the finished tables
- Keep everything version controlled in Git
- Learn to use an AI coding assistant deliberately: write first, review with AI, check every change

## Data
Source: *[dataset name and Kaggle link: add once chosen]*

- License and credit: *[add after checking the dataset page]*
- Collection date: *[add]*

The raw files are not stored in this repo. Download them from Kaggle to run the project.

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
| Claude Code | AI-assisted coding: reviews, explanations, and pair programming |
| Git and GitHub | Version control |

## How I use AI in this project
- I write the first version myself, then use Claude to review, explain, or improve it
- I read every change before accepting it and commit AI-assisted changes separately
- I run `dbt test` and my data checks after every change
- A `CLAUDE.md` file in this repo tells the assistant how the project is organized and what the rules are
- I keep a short log of what worked and what I had to fix (see `notes/ai-log.md`)

## Planned chatbot safeguards
- Read-only database role that can only see the final tables
- Only a single SELECT statement is allowed, with a row limit
- Limited number of questions per session
- A set of test questions with known answers to check the results

## Progress
- [x] Complete GitHub courses (Introduction to GitHub, Introduction to Git, Markdown)
- [ ] Choose a dataset
- [ ] Explore the dataset with pandas
- [ ] Complete Claude Code 101
- [ ] Complete dbt Fundamentals course
- [ ] Add `CLAUDE.md` to the repo
- [ ] Load data into Snowflake
- [ ] Build dbt staging models
- [ ] Use Claude Code to review one dbt model
- [ ] Build dbt marts with tests and documentation
- [ ] Build the chatbot
- [ ] Test the chatbot against known answers
- [ ] Write up what worked and what didn't with AI-assisted coding

## Author
Will. See my [GitHub profile](https://github.com/wclem12) for more about me.
