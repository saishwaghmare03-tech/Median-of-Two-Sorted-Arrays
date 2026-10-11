# Median of Two Sorted Arrays (LeetCode 4)

An optimal Java solution for the classic **Median of Two Sorted Arrays** problem, achieving an **$O(\log(\min(m, n)))$** time complexity using binary search.

---

## 📋 Problem Description

Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the **median** of the two sorted arrays.

The overall run time complexity should be **$O(\log(m+n))$**.

### Examples

* **Example 1:**
  * **Input:** `nums1 = [1, 3]`, `nums2 = [2]`
  * **Output:** `2.00000`
  * **Explanation:** The merged array is `[1, 2, 3]`, and the median is `2`.

* **Example 2:**
  * **Input:** `nums1 = [1, 2]`, `nums2 = [3, 4]`
  * **Output:** `2.50000`
  * **Explanation:** The merged array is `[1, 2, 3, 4]`, and the median is `(2 + 3) / 2 = 2.5`.

---

## 🚀 Approach & Intuition

To satisfy the logarithmic time complexity requirement without merging the entire arrays:
1. **Binary Search on Partitions:** We perform a binary search on the smaller array (`nums1`) to find a correct partition index (`partitionX`).
2. **Complementary Partition:** The partition on the second array (`partitionY`) is automatically calculated so that the left half and right half of the combined partitions contain an equal (or nearly equal) number of elements.
3. **Boundary Validation:** We ensure that every element on the left side is less than or equal to every element on the right side (`maxLeftX <= minRightY` and `maxLeftY <= minRightX`).
4. **Median Calculation:** Once the correct partition is found, the median is calculated based on whether the total number of elements (`m + n`) is odd or even.

---

## ⏱️ Complexity Analysis

* **Time Complexity:** **$O(\log(\min(m, n)))$** — Binary search is performed on the smaller array, yielding logarithmic efficiency.
* **Space Complexity:** **$O(1)$** — Uses a constant amount of extra space for pointers and boundary checks.

---

## 💻 Getting Started / Running the Code

### Prerequisites
Make sure you have the **Java Development Kit (JDK)** installed on your machine.

### Instructions

1. Clone or download the repository files.
2. Save the code into a file named `Solution.java`.
3. Open your terminal or command prompt in the directory containing the file.
4. Compile the code:
   ```bash
   javac Solution.java
