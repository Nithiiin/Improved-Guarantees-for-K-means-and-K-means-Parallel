# Improved Guarantees for k-means++ and k-means++ Parallel

This repository contains the report and supporting materials for the project "Improved Guarantees for k-means++ and k-means++ Parallel" by Nithin Balaji S P and Pulkit R. Khandelwal, conducted as part of the IE 529 course (Stats of Big Data and Clustering) at the University of Illinois, Urbana-Champaign.

## Table of Contents
- [Introduction](#introduction)
- [Technical Background](#technical-background)
- [Key Results](#key-results)
- [Application Example](#application-example)
- [Conclusion](#conclusion)
- [References](#references)
## Introduction
Clustering algorithms, particularly k-means, are essential in data analysis for grouping data points with shared characteristics. The accuracy of k-means is heavily dependent on the initial random selection of cluster centers. This project explores enhancements to the traditional k-means algorithm through k-means++ and its parallel variant to improve clustering quality and scalability.

## Technical Background
- **k-means++ Algorithm**: Improves the initialization phase by carefully selecting initial centroids with specific probabilities.
- **k-means++ Parallel**: A scalable version that initializes centroids over multiple rounds to handle large datasets efficiently.

## Key Results
- The k-means++ algorithm reduces the predicted approximation factor from 8(ln k + 2) to a smaller bound, resulting in better performance guarantees.
- The k-means++ parallel algorithm demonstrates significant cost savings with proper configuration and iteration rounds.

## Application Example
Data used: D31 dataset with 3100 rows of 2-dimensional data, grouped into 31 clusters.

- **Total Cost of Clustering**:
  - k-means++: 11264.5092
  - k-means++ Parallel: 8758.94
  - k-means++ Parallel_pois: 8331.6

## Conclusion
The k-means++ and k-means++ parallel algorithms enhance clustering methodologies by refining initialization steps and integrating parallel processing capabilities, leading to improved clustering quality, faster convergence, and better scalability for large datasets.

## References
1. Arthur, D., & Vassilvitskii, S. (2007). k-means++: The advantages of careful seeding. Proceedings of the eighteenth annual ACM-SIAM symposium on Discrete algorithms.
2. Bahmani, B., Moseley, B., Vattani, A., Kumar, R., & Vassilvitskii, S. (2012). Scalable k-means++. Proceedings of the VLDB Endowment.
3. Other references listed in the report.
