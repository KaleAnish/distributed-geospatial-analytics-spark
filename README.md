# distributed-geospatial-analytics-spark
Distributed geospatial data processing pipeline using Apache Spark and Sedona, with Hilbert curve–based spatial indexing and large-scale JSON stream processing.

## Overview

This project implements a distributed spatio-temporal data processing pipeline using Apache Spark and Apache Sedona. It demonstrates large-scale geospatial data handling, spatial indexing via Hilbert curve mapping, and schema inference for semi-structured JSON data.

The project was developed as part of Advanced DBMS (CS236) and focuses on scalable data processing and spatial analytics.

---

## Technologies Used

- Apache Spark (RDD + DataFrame APIs)
- Apache Sedona (Spatial extension for Spark)
- PySpark
- Hilbert Curve spatial indexing
- JSON schema inference
- Geospatial data processing

---

## Part 1: Earthquake Geospatial Processing

Dataset: Earthquake dataset (Kaggle)

Steps:
- Loaded CSV geospatial data into Spark
- Converted to SpatialRDD using Sedona
- Applied spatial partitioning
- Normalized latitude/longitude to fixed grid
- Implemented Hilbert curve transformation to map 2D spatial coordinates to 1D index
- Generated transformed dataset for efficient spatial querying

### Key Concept

Hilbert curve mapping preserves spatial locality while enabling 1D indexing of 2D geospatial coordinates — useful for distributed storage and range queries.

---

## Part 2: Twitter JSON Stream Processing

Dataset: Raw Twitter JSON stream data

Steps:
- Parsed large JSON text dataset
- Inferred nested schema using Spark
- Processed semi-structured data using DataFrame API
- Enabled scalable querying of structured + semi-structured data

---

## Technical Highlights

- Implemented spatial indexing logic manually
- Worked with both RDD and DataFrame paradigms
- Handled nested JSON schema in distributed environment
- Configured Spark and Sedona runtime environment
- Designed pipeline for scalable geospatial analytics

---

## Potential Extensions

- Spatial range queries and nearest-neighbor queries
- Time-window based spatio-temporal analytics
- Benchmarking partitioning strategies
- Integration with distributed storage (S3/HDFS)

---

## License

MIT License
