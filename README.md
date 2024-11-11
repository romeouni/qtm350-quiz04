# QTM 350 - Quiz 04

## SQL Queries

In this quiz, you will test your SQL skills through queries using two tables. The tables refer to Nobel Prize winners and their respective personal information. The data and questions are available in the `quiz04.sql` file. The tables are as follows.

### Table Structures

#### nobel_laureates

This table contains personal and award information about Nobel Prize winners:

| Column        | Type          | Description                                    |
|---------------|---------------|------------------------------------------------|
| id            | SERIAL        | Primary key                                    |
| name          | VARCHAR(100)  | Full name of the laureate                      |
| field         | VARCHAR(50)   | Field of study (Physics, Chemistry, Physiology)|
| year_award    | INT           | Year the Nobel Prize was awarded               |
| prize_amount  | DECIMAL(12,2) | Prize amount in USD                            |
| age_at_award  | INT           | Age of the laureate when receiving the award   |

#### discoveries

This table contains information about the laureates' groundbreaking discoveries:

| Column          | Type          | Description                                    |
|-----------------|---------------|------------------------------------------------|
| id              | SERIAL        | Primary key                                    |
| laureate_id     | INT           | Foreign key referencing nobel_laureates(id)    |
| discovery       | VARCHAR(255)  | Description of the scientific discovery        |
| year_discovery  | INT           | Year when the discovery was made               |
| research_funding| DECIMAL(12,2) | Amount of funding received for the research    |
| citation_count  | INT           | Number of citations for the discovery          |

### Relationships

- Each laureate in `nobel_laureates` has exactly one corresponding discovery in the `discoveries` table
- The tables are linked through the `laureate_id` foreign key in the `discoveries` table

### Deliverables

You may use any SQL client of your choice to write and test your queries, including [pgAdmin](https://www.pgadmin.org/), the [SQL Notebook extension for VS Code](https://marketplace.visualstudio.com/items?itemName=cmoog.sqlnotebook), [SQLite](https://www.sqlite.org/index.html), [`sqlalchemy`](https://www.sqlalchemy.org/), or online editors like [SQLite Online](https://sqliteonline.com/).

Please submit only your `.sql` file containing the queries on Canvas.

Good luck! 😉