

# Large Scale Data Processing: Project 2



### 1. Exact F2 Algorithm
- **Task:** Implement the `exact_F2` function to calculate the exact F2 value.
- **Results:**
  - Local Execution: ![Local Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/4d1374b2-d5aa-4712-bb08-6ce2993df657)
  - GCP Execution: ![GCP Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/80e7669a-3a24-4c97-ba33-d553b16d8930)
  - Note: Execution on GCP was surprisingly slower.

### 2. Tug-of-War Algorithm
- **Task:** Implement the `Tug_of_War` function with specified parameters.
- **Results:**
  - Local Execution: ![Local Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/a7f398ca-a7b6-4ee7-b5e0-607dd63c0801)
  - GCP Execution: ![GCP Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/d6644010-5425-4363-b294-c692531619d8)

### 3. BJKST Algorithm
- **Task:** Implement the `BJKST` function to estimate F0 with the smallest `width` achieving an error of +/- 20%.
- **Results:**
  - Local Execution: ![Local Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/e76d68e1-d7ca-414e-8930-c195bbda99cf)
  - GCP Execution: ![GCP Execution Result](https://github.com/kelseyzeng0610/project_2/assets/78379458/679bc6af-ecdc-41df-b13f-4ceb8e3bbd72)

### 4. Algorithm Comparison
- **BJKST vs. Exact F0:**
  - BJKST Estimate: 8,388,608
  - Exact F0: 7,406,649
  - The BJKST algorithm with 80 buckets and 5 trials provided a slightly higher estimate than the exact F0 value. The error of 13.3% is within an acceptable range.
- **Tug-of-War vs. Exact F2:**
  - Tug-of-War Estimate: 7,300,978,582
  - Exact F2: 8,567,966,130
  - The Tug-of-War algorithm's estimate is lower than the exact F2 value. The parameters may require further tuning.

### Summary
The BJKST algorithm can provide a relatively accurate estimate for the distinct count problem with carefully chosen parameters. It offers a trade-off between accuracy and computational efficiency compared to the exact computation.
The Tug-of-War algorithm, on the other hand, may require more careful parameter tuning to achieve a closer approximation for the F2 problem. The algorithm itself also took a long time to run on GCP/Local Machine, possibly due to the computational complexity of maintaining multiple sketches.

## Contributors
Kelsey Zeng, Zihan Ni, Peiyu Zhong
