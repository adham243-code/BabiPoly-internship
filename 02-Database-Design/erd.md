 # Database Design (ERD)

## 1. Entities

### Users

* id (Primary Key)
* name
* email
* password
* created_at
* updated_at

### Games

* id (Primary Key)
* name
* created_at
* updated_at

### Scores

* id (Primary Key)
* user_id (Foreign Key → users.id)
* game_id (Foreign Key → games.id)
* score
* created_at
* updated_at

---

## 2. Relationships

* A User can have many Scores (1:N)
* A Game can have many Scores (1:N)
* Each Score belongs to one User and one Game

---

## 3. Description

The database is designed to support an online gaming platform where users can participate in different games and record their scores. The Scores table acts as a bridge between Users and Games, allowing tracking of performance for each user in each game.