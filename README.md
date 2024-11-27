# MovieLens Similarity Analysis 🎥✨

## Project Overview
This project demonstrates a **Big Data analysis** using **Apache Spark** on the **MovieLens 10M dataset**. The goal is to calculate similarity scores between movies using **cosine similarity** based on user ratings, highlighting data engineering and analytical skills for distributed systems.

**Key Features**:
- Calculated cosine similarity to identify movies most similar to *Toy Story (1995)*.
- Utilized **AWS EMR** and **PySpark** for scalable distributed data processing.
- Processed large-scale datasets from S3, leveraging Spark for efficient computation.

---

## Dataset Description
The **MovieLens 10M Dataset** includes:
- **Ratings Data**: User ratings for 10 million movie-user pairs.
- **Movies Data**: Movie titles and genres.

**Source**: [Kaggle MovieLens 10M Dataset](https://www.kaggle.com/datasets/smritisingh1997/movielens-10m-dataset?resource=download)

---

## Project Workflow
### Tools and Technologies
- **Apache Spark**: Distributed data processing framework.
- **PySpark**: Python API for Spark.
- **AWS EMR**: Managed cluster for running Spark jobs.
- **S3**: Cloud storage for data files.

### Implementation Steps
1. **Data Preparation**:
   - Loaded `movies.dat` and `ratings.dat` from S3 into PySpark DataFrames.
   - Joined user ratings with movie metadata to create a unified dataset.

2. **Similarity Calculation**:
   - Applied **cosine similarity** to compute relationships between *Toy Story (1995)* and other movies.
   - Used co-rating filters (minimum 10 users) for robust similarity metrics.

3. **Output**:
   - Displayed the top 10 most similar movies to *Toy Story (1995)*.

---

## Example Output
Here’s a sample of the output:

| **Movie Name**      | **Similar Movies**         | **Score**   |
|---------------------|----------------------------|-------------|
| Toy Story (1995)    | In Old Chicago (1937)      | 0.9966      |
| Toy Story (1995)    | Marooned in Iraq (2002)    | 0.9947      |
| Toy Story (1995)    | They Died with Their Boots On (1941) | 0.9930 |

---

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/bhutto17/MovieSimilarity-Analysis.git
   cd MovieLens-Similarity-Analysis
