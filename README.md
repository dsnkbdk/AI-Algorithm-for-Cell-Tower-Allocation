# AI Algorithm for Cell Tower Allocation

This project aims to develop an algorithm to systematically allocate cell towers to different core network hubs to mitigate service impact. The project explores and implements two primary methods, clustering and map coloring with iterative optimization, to achieve effective allocation while balancing the load and minimizing the number of hubs.

## Introduction

In the era of smartphones, signal coverage is directly related to user experience. This project aims to develop algorithms for allocating cell towers to different core network hubs, thus mitigating service impact in case of hub faults. The project approaches this problem from a computer science perspective, employing clustering and map coloring algorithms.

## Objectives

1. To define an effective distance measure and adjacency relationship for cell towers.
2. To develop and test algorithms for the systematic allocation of cell towers to hubs.
3. To ensure load balancing and minimize the number of hubs while maintaining effective coverage.
4. To provide a scalable solution that can be expanded beyond the initial test region.

## Methodology

### Data Preprocessing

- **Missing Values:** Filled using geographical information.
- **Duplicate Values:** Removed based on predefined rules.
- **Outliers:** Corrected using known geographical information.
- **Standardization:** Ensured consistent formatting.
- **Data Splitting:** Separated data for Florida and entire U.S.

### Geographic Distance Calculation

A custom function was developed to calculate the geographical distance between cell towers, considering the curvature of the Earth.

### Methods

#### Method 1: Clustering Algorithm

Uses k-means clustering to divide cell towers into clusters. Each cluster is then assigned to different hubs, ensuring that no two adjacent towers are connected to the same hub.

#### Method 2: Map Coloring Algorithm with Iterative Optimization

Transforms the allocation problem into a map coloring problem, ensuring adjacent towers are assigned to different hubs. Iterative optimization reduces the number of hubs and balances the load.

## Results

### Florida Data

- **Clustering Algorithm:** Efficiently divided cell towers into clusters but resulted in load imbalances.
- **Map Coloring Algorithm:** Effectively assigned adjacent towers to different hubs. Iterative optimization further balanced the load and reduced the number of hubs.

### Entire U.S. Data

Similar results were observed with both methods when applied to the entire U.S. dataset. Method 2 showed better performance in load balancing and minimizing the number of hubs.

## Analysis

Both methods were analyzed for their effectiveness, load balancing, and scalability. Method 1 was found to be quicker but less balanced, while Method 2 provided more precise allocation and better load management.

## Discussion

Method 1 is recommended for quick and rough allocation with limited resources. Method 2, while more complex, offers better accuracy and scalability, making it suitable for future expansions.

## Conclusion

The project successfully developed two methods for cell tower allocation. Method 2 is recommended for its flexibility and better performance in load balancing and minimizing the number of hubs.

## Future Work

- Improving iterative optimization algorithms.
- Relaxing county-based constraints for more flexible hub allocation.
- Combining clustering and map coloring for better results.

## References

- L. Sauras-Altuzarra, “Adjacency Matrix,” MathWorld, 2023.
- A. Simmons, “What is a Cell Tower? Understanding How Cell Towers Work,” DGTL Infra, 2023.
- G. Seif, “The 5 Clustering Algorithms Data Scientists Need to Know,” Towards Data Science, 2018.
- M. Sahu, “A Classical Constraint Satisfaction Problem and its Solution using Artificial Intelligence,” AICAI, 2019.

For the complete source code, please refer to the file `Project.Rmd`.
