<img width="1542" height="1018" alt="image" src="https://github.com/user-attachments/assets/759c77a3-f68d-40b8-b828-173bbcc221ae" />
Configuration placeholder
from utils import square, is_even, celsius_to_fahrenheit, greet

def main():
    s = input("Enter a number: ")
    try:
        n = float(s)
    except ValueError:
        print("Invalid input: please enter a number")
        return

    sq = square(n)
    even = is_even(n)
    f = celsius_to_fahrenheit(n)

    print(f"Square: {sq}")
    print("Even" if even else "Odd")
    print(f"{n}C = {f}F")

    name = input("Enter your name for a greeting: ")
    if name:
        print(greet(name))
def square(n):
    return n * n

def is_even(n):
    try:
        return int(n) % 2 == 0
    except Exception:
        return False

def celsius_to_fahrenheit(c):
    return (c * 9/5) + 32

def greet(name):
    return f"Hello, {name}!"  _pycache__/
*.pyc
.env
if __name__ == '__main__':
    main()
# Product Catalog with MongoDB, Redis, and PostgreSQL (pgvector)

## Project Overview

This project demonstrates how to build a modern e-commerce product catalog using three different databases, each serving a specific purpose:

- **MongoDB** – Stores product information as flexible documents.
- **Redis** – Caches frequently accessed products and manages leaderboards.
- **PostgreSQL with pgvector** – Performs semantic search using vector embeddings.

This architecture reflects real-world production systems where multiple databases are combined to improve performance, scalability, and search capabilities.

---

## Technologies Used

- MongoDB
- Redis
- PostgreSQL
- pgvector
- Python
- PyMongo
- redis-py
- psycopg2
- Git
- GitHub

---

## Project Structure

```
product-catalog/
│
├── mongodb/
│   ├── insert_products.py
│   ├── queries.py
│
├── redis/
│   ├── cache.py
│   ├── leaderboard.py
│
├── postgres/
│   ├── create_tables.sql
│   ├── semantic_search.py
│
├── screenshots/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Features

- Store product information in MongoDB.
- Query products using MongoDB filters.
- Cache popular products with Redis.
- Build product popularity leaderboards.
- Store product embeddings in PostgreSQL.
- Perform semantic similarity searches using pgvector.

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/product-catalog.git
```

### 2. Navigate into the project

```bash
cd product-catalog
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Database Setup

### MongoDB

Start MongoDB and create a database named:

```
product_catalog
```

---

### Redis

Start the Redis server.

Example:

```bash
redis-server
```

---

### PostgreSQL

Create a database:

```sql
CREATE DATABASE product_catalog;
```

Enable the pgvector extension:

```sql
CREATE EXTENSION vector;
```

---

## Running the Project

### MongoDB

Insert products:

```bash
python mongodb/insert_products.py
```

Run queries:

```bash
python mongodb/queries.py
```

---

### Redis

Run cache example:

```bash
python redis/cache.py
```

Run leaderboard:

```bash
python redis/leaderboard.py
```

---

### PostgreSQL

Create tables:

```bash
psql -d product_catalog -f postgres/create_tables.sql
```

Run semantic search:

```bash
python postgres/semantic_search.py
```

---

## Example Product

```json
{
    "name": "Wireless Mouse",
    "category": "Electronics",
    "price": 25.99,
    "brand": "Logitech",
    "stock": 100
}
```

---

## Learning Objectives

This project demonstrates:

- Document databases using MongoDB.
- In-memory caching with Redis.
- Semantic search using PostgreSQL and pgvector.
- Multi-database architecture.
- Basic CRUD operations.
- Efficient data retrieval.

---

## Screenshots

Add screenshots here showing:

- MongoDB documents
- Redis cache
- PostgreSQL tables
- Semantic search results
- Terminal outputs

---

## Author

**Name:** Gloria Tago

---

## License

This project is for educational purposes as part of a hands-on database lab.
