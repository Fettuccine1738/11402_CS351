# 11402_CS351_ProjectB
# CSV Mini Database & Query Engine

## Overview

This project implements a lightweight database engine over CSV files. It focuses on parsing, indexing, and executing simple queries, demonstrating core database concepts without relying on a full DBMS.

---

## Objectives

* Parse CSV files (including quoted fields)
* Build indexes for efficient data access
* Design and implement a simple query grammar
* Explore performance trade-offs between different query strategies

---

## Features

* CSV file ingestion
* Robust parsing (handles quoted fields and delimiters)
* Simple query language (SQL-like)
* Optional indexing for faster queries
* Configurable parsing approach (custom or library-based)

---

## CSV Parsing

Two approaches are supported:

### 1. Custom Parser

* Handles:

  * Quoted fields (`"a,b"`)
  * Escaped quotes (`""`)
  * Delimiters inside quotes
* Useful for learning and full control

### 2. Library-Based Parser (Optional)

* Can use external libraries via:

  * `vcpkg`
  * `Conan`
* Reduces implementation complexity

---

## Query Language

A minimal SQL-inspired syntax is supported:

```
SELECT <columns> FROM <file>
SELECT <columns> FROM <file> WHERE <condition>
```

### Examples

```
SELECT * FROM data.csv
SELECT name, age FROM data.csv
SELECT name FROM data.csv WHERE age > 30
SELECT city FROM data.csv WHERE country = "Japan"
```

### Supported Operators

* `=`
* `!=`
* `<`, `>`
* `<=`, `>=`

---

## Indexing

Indexes can be built to improve query performance.

### Strategies

* **Hash-based index**

  * Fast lookups for equality conditions
* **Tree-based index (optional)**

  * Supports range queries

### Trade-offs

* Faster queries vs increased memory usage
* Index build time vs query speed

---

## Execution Flow

1. Load CSV file
2. Parse data into memory
3. Build indexes (optional)
4. Parse query
5. Execute query
6. Output results

---

## Performance Considerations

| Approach      | Advantage    | Disadvantage                |
| ------------- | ------------ | --------------------------- |
| Full Scan     | Simple       | Slow for large datasets     |
| Indexed Query | Fast lookups | Extra memory + build cost   |
| Hybrid        | Balanced     | More complex implementation |

---

## Build & Run

### Compile

```
g++ -std=c++17 -Iinclude src/main.cpp -o csv_db
```

### Run

```
./csv_db
```

---

## Future Work

* Support for `AND` / `OR` conditions
* Multi-file queries (JOINs)
* Persistent indexes (disk storage)
* Interactive CLI
* Streaming large CSV files

---

## License

MIT License
