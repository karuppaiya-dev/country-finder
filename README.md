# 🌍 Country Finder

A web application that lets you search for any country and highlights it on an interactive world map.

## ✨ Features

- 🔍 Search any country by name
- 🗺️ Highlights the country on an interactive SVG world map
- 🎯 Smart search — handles partial names, extra words, and special characters

## 🛠️ Tech Stack

- **Backend** — Node.js, Express
- **Frontend** — EJS, HTML, CSS
- **Database** — PostgreSQL

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/karuppaiya-dev/country-finder.git
cd country-finder
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup PostgreSQL Database
Make sure PostgreSQL is running and follow these steps:

**Step 1 — Create the database:**
```sql
CREATE DATABASE world;
```

**Step 2 — Create the table:**
```sql
CREATE TABLE countries (
  country_code VARCHAR(10),
  country_name VARCHAR(100)
);
```

**Step 3 — Import `countries.csv`:**
```sql
\copy countries(country_code, country_name) 
FROM '/path/to/countries.csv' 
DELIMITER ',' 
CSV HEADER;
```

> Replace `/path/to/countries.csv` with the actual path of your file.  
> Example: `FROM 'C:/Users/karuppaiya/Desktop/countries.csv'`

**Step 4 — Verify the import:**
```sql
SELECT * FROM countries LIMIT 5;
```

### 4. Create `.env` file
Create a `.env` file in the root of the project:
```
DB_USER=postgres
DB_HOST=localhost
DB_NAME=world
DB_PASSWORD=your_password_here
DB_PORT=5432
```

### 5. Run the app
```bash
node index.js
```

Open your browser and go to `http://localhost:3000`

## 📁 Project Structure

```
country-finder/
├── public/
│   └── styles/
├── views/
│   └── index.ejs
├── index.js
├── countries.csv
├── .env
├── .gitignore
└── README.md
```

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `DB_USER` | PostgreSQL username |
| `DB_HOST` | Database host |
| `DB_NAME` | Database name |
| `DB_PASSWORD` | Database password |
| `DB_PORT` | Database port |

## 👤 Author

**Karuppaiya Murugan**  
GitHub: [@karuppaiya-dev](https://github.com/karuppaiya-dev)
