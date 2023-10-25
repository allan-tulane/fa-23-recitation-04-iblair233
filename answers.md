# CMPS 2200 Recitation 5
## Answers

**Name:** Izzy Blair


Place all written answers from `recitation-05.md` here for easier grading.







- **1b.**
- Results for randomized list:
|      n |   qsort-fixed-pivot |   qsort-random-pivot |  selection-sort |
|--------|---------------------|----------------------|-----------------|
|    100 |               0.155 |                0.124 |           0.013 |
|    200 |               0.271 |                0.268 |           0.299 |
|    500 |               0.770 |                0.760 |           0.800 |
|   1000 |               1.760 |                1.893 |           1.987 |
|   2000 |               3.814 |                3.696 |           4.133 |
|   5000 |              10.214 |               10.033 |          10.244 |
|  10000 |              21.820 |               21.596 |          23.997 |
|  20000 |              46.980 |               47.519 |          87.542 |
|  50000 |             129.930 |              132.189 |         198.775 |
| 100000 |             269.306 |              278.606 |         302.543 |

The quicksort methds are faster than the selection sort methods when the list is randomized.

Results for sorted list:
|      n |   qsort-fixed-pivot |   qsort-random-pivot |  selection-sort |
|--------|---------------------|----------------------|-----------------|
|    100 |               0.336 |                0.123 |           0.013 |
|    200 |               0.312 |                0.309 |           0.028 |
|    500 |               0.773 |                0.804 |           0.768 |
|   1000 |               1.992 |                1.932 |           0.985 |
|   2000 |               3.812 |                3.776 |           3.821 |
|   5000 |               9.651 |                9.594 |           9.455 |
|  10000 |              20.904 |               20.777 |          20.801 |
|  20000 |              45.361 |               46.085 |          45.918 |
|  50000 |             120.811 |              122.550 |         121.543 |
| 100000 |             259.808 |              268.556 |         262.749 |

For a sorted list, it seems that selection sort was usually faster than random pivot qsort but slower than fixed pivot quicksort. However, the selection sort for a sorted list is still faster than the selection sort for the randomized list.

Selection sort has a work of O(n^2). the worst case work for quicksort is O(n^2) and the best case work is O(nlogn). If the list is sorted, then the fastest is fixed pivot quicksort. if the list is not sorted, the quicksort is faster than selection sort.

- **1c.**
For a sorted list, the fastes function is quicksort with a random pivot. See below the comparisons to python's sorted functions:
|      n |   qsort-random-pivot |   tim-sort |
|--------|----------------------|------------|
|    100 |                0.144 |      0.120 |
|    200 |                0.276 |      0.269 |
|    500 |                0.789 |      0.840 |
|   1000 |                1.883 |      1.841 |
|   2000 |                3.625 |      3.572 |
|   5000 |                9.760 |      9.535 |
|  10000 |               22.040 |     21.951 |
|  20000 |               50.204 |     48.293 |
|  50000 |              124.310 |    125.894 |
| 100000 |              254.066 |    257.545 |

For sorted lists, we can see tim sort is usually faster than quicksort.

For randomized list the fastest is quicksort with a fixed pivot. See below results:

|      n |   qsort-fixed-pivot |   tim-sort |
|--------|---------------------|------------|
|    100 |               0.168 |      0.138 |
|    200 |               0.288 |      0.283 |
|    500 |               0.777 |      0.771 |
|   1000 |               1.739 |      1.766 |
|   2000 |               3.854 |      3.899 |
|   5000 |              10.425 |     10.587 |
|  10000 |              22.914 |     22.931 |
|  20000 |              51.988 |     51.119 |
|  50000 |             129.122 |    126.661 |
| 100000 |             277.081 |    292.315 |

Tim sort is slower for a randomized list than it is for a sorted list, but it is still faster than quicksort.
