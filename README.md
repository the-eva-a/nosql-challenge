# NoSQL Challenge: UK Food Standards Agency Analysis

## Project Overview
This project is part of the Module 12 NoSQL Challenge for my data analytics bootcamp. The objective is to analyze UK Food Standards Agency ratings data using MongoDB and PyMongo to support the editorial team of 'Eat Safe, Love' magazine.

## Repository Structure
```
nosql-challenge/
├── NoSQL_setup.ipynb  # Database setup and modifications
├── NoSQL_analysis.ipynb  # Data analysis and queries
└── Resources/
    └── establishments.json  # Provided dataset
```

## Database Setup and Data Import
- Database Name: `uk_food`
- Collection Name: `establishments`
- Data Import Command:
```bash
mongoimport --db uk_food --collection establishments --file Resources/establishments.json --jsonArray
```

## Database Modifications
- **Added New Restaurant:** 'Penang Flavours' (Greenwich)
- **Updated BusinessTypeID for Restaurants**
- **Removed Establishments in Dover**
- **Converted Coordinates (`latitude`, `longitude`) to Numbers**
- **Converted `RatingValue` to Integers**

## Exploratory Analysis Queries
1. **Hygiene Score of 20:** Count and display establishments.
2. **London Establishments with Rating >= 4:** Filter using regex.
3. **Top 5 Establishments Near 'Penang Flavours' with Rating 5:** Sorted by hygiene score.
4. **Top 10 Local Authorities with Hygiene Score 0:** Grouped and sorted using aggregation.

## Results Summary
- Successfully inserted and verified the new restaurant.
- Removed all establishments from Dover.
- Corrected number types for coordinates and ratings.
- Performed analytical queries to support editorial decisions.

## Technologies Used
- **MongoDB:** Database management and querying.
- **PyMongo:** Python library for interacting with MongoDB.
- **Pandas:** Data manipulation and display.
- **Jupyter Notebook:** Interactive code execution and documentation.

## Acknowledgements
---
This project is part of the curriculum in the edX Data Analytics Bootcamp. Special thanks to my instructors and peers for their support and guidance.