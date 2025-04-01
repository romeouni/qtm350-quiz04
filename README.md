# QTM 350 - Quiz 04

## SQL Queries

In this quiz, you will test your SQL skills through queries using two tables. The tables refer to Nobel Prize winners and their respective personal information. The data and questions are available in the `quiz04.ipynb` file. The tables are as follows.

### Table Structures

#### nobel_laureates

This table contains personal and award information about Nobel Prize winners:

| Column        | Type          | Description                                    |
|---------------|---------------|------------------------------------------------|
| id            | INTEGER       | Primary key (auto-increments in SQLite)        |
| name          | TEXT          | Full name of the laureate                      |
| field         | TEXT          | Field of study (Physics, Chemistry, Physiology)|
| year_award    | INTEGER       | Year the Nobel Prize was awarded               |
| prize_amount  | REAL          | Prize amount in USD                            |
| age_at_award  | INTEGER       | Age of the laureate when receiving the award   |

#### discoveries

This table contains information about the laureates' groundbreaking discoveries:

| Column          | Type          | Description                                    |
|-----------------|---------------|------------------------------------------------|
| id              | INTEGER       | Primary key (auto-increments in SQLite)        |
| laureate_id     | INTEGER       | Foreign key referencing nobel_laureates(id)    |
| discovery       | TEXT          | Description of the scientific discovery        |
| year_discovery  | INTEGER       | Year when the discovery was made               |
| research_funding| REAL          | Amount of funding received for the research    |
| citation_count  | INTEGER       | Number of citations for the discovery          |

### Relationships

- Each laureate in `nobel_laureates` has exactly one corresponding discovery in the `discoveries` table
- The tables are linked through the `laureate_id` foreign key in the `discoveries` table

### Deliverables

Please submit only your `.ipynb` file containing the queries on Canvas.

Good luck! 😉