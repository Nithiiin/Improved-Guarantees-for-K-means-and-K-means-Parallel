# Improved Guarantees for k-means++ and k-means++ Parallel

This repository contains the report and supporting materials for the project "Improved Guarantees for k-means++ and k-means++ Parallel"

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
1. **Improving k-means++ Guarantees**:
   - The estimated cost of the k-means++ algorithm's solution is no more than 5(ln k + 2) times the cost of the best solution.
   - The new bound for the estimated cost of a cluster covered at stage t+1 is improved to 5 OPT1(Pi), where OPT1(Pi) denotes the optimal cost of clustering Pi with one center.

2. **Bi-Criteria Approximation**:
   - The k-means++ algorithm's performance improves when additional centers beyond the standard k are used.
   - Notable improvements in approximation guarantees are achieved when the oversampling parameter Δ is relatively small.

3. **Parallel k-means++ Algorithm Analysis**:
   - The k-means++ parallel algorithm provides upper bounds for predicted clustering cost, maintaining an approximation to the optimal clustering solution.
   - After T rounds, the predicted clustering cost is no more than nine times the optimal clustering cost.

4. **Algorithm Complexity**:
   - The seeding phase of k-means++ has a time complexity of O(nk), where n is the number of data points and k is the number of clusters.
   - k-means++ parallel has a complexity of O(T⋅n⋅l), where T is the number of passes and l is a parameter defining the number of centers chosen per round.

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
