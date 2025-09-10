# 🎬 Final-SQL-Project-FILM_INDUSTRY  

<img width="820" height="547" alt="image" src="https://github.com/user-attachments/assets/02e01142-dcc8-4454-b1d3-0692e623f7cf" />



## 📌 Overview  
The **Final-SQL-Project-FILM_INDUSTRY** is a comprehensive SQL database project that models the real-world structure of the global film industry.  
It focuses on **relational design, normalization, data integrity, and query optimization**, offering a complete simulation of how films, actors, studios, theaters, and revenues interact in practice.  

This project is ideal for **students, educators, data analysts, and SQL enthusiasts** who want to explore advanced database design and analysis within the entertainment domain.  

---

## 🏗️ Features  
- ✅ **25 well-structured tables** with 10 attributes each  
- ✅ **Primary & foreign keys** ensuring referential integrity  
- ✅ **Normalized design (up to 3NF)** for data consistency  
- ✅ **Realistic, human-friendly sample datasets**  
- ✅ **Optimized SQL queries** for deep insights  
- ✅ **Covers multiple domains of the film industry**, including:  
  - Film Information (titles, genres, languages, release details)  
  - Cast & Crew (actors, directors, producers, writers)  
  - Studios & Production Houses  
  - Theaters & Distribution Channels  
  - Awards & Film Festivals  
  - Financials (budgets, revenues, profits, investors)  
  - Streaming & Digital Media Platforms  

---

## 📂 Database Structure  
The project contains **25 interconnected tables**, including:  

- 🎥 `films` – Film details such as title, genre, language, and release date  
- 👥 `actors` – Actor profiles and filmography  
- 🎬 `directors` – Director details and career highlights  
- 🏢 `studios` – Production houses and ownership records  
- 🎟️ `theaters` – Theater locations and screening schedules  
- 🏆 `awards` – Nominations and winners of major festivals  
- 💰 `box_office` – Budgets, revenue, and profit data  
- 📡 `streaming_platforms` – OTT licensing and subscriber stats  

---

## 📊 Example Queries  
Some advanced SQL queries included in this project:  

```sql
-- Top 5 highest-grossing films by year
SELECT title, release_year, revenue
FROM films
ORDER BY revenue DESC
LIMIT 5;

-- Actor–Director collaboration count
SELECT a.actor_name, d.director_name, COUNT(f.film_id) AS total_films
FROM films f
JOIN actors a ON f.actor_id = a.actor_id
JOIN directors d ON f.director_id = d.director_id
GROUP BY a.actor_name, d.director_name
ORDER BY total_films DESC;
