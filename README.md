# 📽️ Movie Recommendation System using Ploomber and DuckDB

This project is a **modular and scalable Movie Recommendation System** built using [Ploomber](https://ploomber.io/) for pipeline orchestration and [DuckDB](https://duckdb.org/) for efficient in-process analytics. It demonstrates how modern data tools can be combined to build a **fast, lightweight, and reproducible machine learning pipeline** for content-based movie recommendations.

---

## 🔧 Tech Stack

- **Ploomber** – For defining, orchestrating, and running modular data pipelines.
- **DuckDB** – An in-process SQL OLAP database optimized for analytical workloads.
- **Python** – Core language for data processing and modeling.
- **scikit-learn** – For building and training the recommendation model.
- **FastAPI** – For serving the model via a lightweight REST API (if included).
- **Docker** – For containerized deployment and reproducibility.

---

## 💡 Features

- Cleans and transforms raw movie metadata.
- Generates movie embeddings using TF-IDF on genres, overviews, and more.
- Computes cosine similarity for movie recommendations.
- Returns top-N similar movies for a given title.
- Powered by SQL queries on DuckDB for fast, memory-efficient processing.
- Modular pipeline with Ploomber for easy debugging, testing, and extension.

---

## 🚀 Use Case

This system is ideal for:
- Small to medium-scale movie recommendation tasks
- Educational purposes in data science and ML pipelines
- A starting point for building more advanced recommender systems using collaborative filtering or deep learning




## Set up - with Docker

```
docker build -t movierec:latest -f Dockerfile .

docker run -it -p 8000:8000 movierec:latest

```
## Explore container

Open new terminal window & ```docker ps``` & copy container id

docker ```docker exec -ti YOURCONTAINERID /bin/bash```

```./movies_data.duckdb```

Explore the database


## Navigate to Browser

Navigate to ```http://localhost:8000``` in browser

Navigate to ```http://localhost:8000/docs``` in browser


## Set up - one step at a time

1. Create new environment

```
conda create --name poetry-env python=3.10
```

2. Activate environment

``` 
conda activate poetry-env
```

3. Install poetry

```
pip install poetry
```

4. Install dependencies

```
poetry lock
poetry install
```

5. Run the as a Ploomber pipeline

```
cd mini-projects/
poetry run ploomber build
```

