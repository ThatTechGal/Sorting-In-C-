# Sorting-In-C-
Sorting Algorithms in C++


🫧 1. Bubble Sort
Idea:
Compare adjacent elements and swap them if they are in the wrong order. Largest values "bubble" to the end with each pass.

Step-by-Step (Example: [5, 3, 8, 4, 2])
First Pass:

Compare 5 and 3 → swap → [3, 5, 8, 4, 2]

Compare 5 and 8 → ok

Compare 8 and 4 → swap → [3, 5, 4, 8, 2]

Compare 8 and 2 → swap → [3, 5, 4, 2, 8]

Second Pass:

Compare 3 and 5 → ok

Compare 5 and 4 → swap → [3, 4, 5, 2, 8]

Compare 5 and 2 → swap → [3, 4, 2, 5, 8]

Keep repeating... until no swaps are needed.



🔍 2. Selection Sort
Idea:
Repeatedly find the smallest (or largest) element and move it to the front.

Step-by-Step (Example: [5, 3, 8, 4, 2])
First Pass:

Find smallest → 2 → swap with first → [2, 3, 8, 4, 5]

Second Pass:

Find smallest in [3, 8, 4, 5] → 3 → already in place

Third Pass:

Find smallest in [8, 4, 5] → 4 → swap with 8 → [2, 3, 4, 8, 5]

Keep going until sorted.



✍️ 3. Insertion Sort
Idea:
Take one element at a time and insert it into its correct position in the sorted part of the array.

Step-by-Step (Example: [5, 3, 8, 4, 2])
Start with 5 (already "sorted")

Take 3:

Compare with 5 → 3 is smaller → move 5, insert 3 → [3, 5, 8, 4, 2]

Take 8:

Compare with 5 → bigger → stay → [3, 5, 8, 4, 2]

Take 4:

Compare with 8 → move 8

Compare with 5 → move 5

Compare with 3 → stop → insert 4 → [3, 4, 5, 8, 2]

Take 2:

Insert at beginning → [2, 3, 4, 5, 8]



🧬 4. Merge Sort (Divide & Conquer)
Idea:
Divide the array into halves

Sort each half

Merge the sorted halves back together

Step-by-Step (Example: [5, 3, 8, 4, 2])
Split:

[5, 3, 8] and [4, 2]

[5], [3, 8] → then [3] and [8]

[4], [2]

Merge Back:

Merge [3] and [8] → [3, 8]

Merge [5] and [3, 8] → [3, 5, 8]

Merge [4] and [2] → [2, 4]

Merge [3, 5, 8] and [2, 4] → [2, 3, 4, 5, 8]



⚡ 5. Quick Sort (Divide & Conquer)
Idea:
Pick a "pivot" element, partition the array so that:

Left has elements < pivot

Right has elements > pivot Then recursively sort both sides.

Step-by-Step (Example: [5, 3, 8, 4, 2])
Choose Pivot (e.g., 2):

Partition → [2, 3, 8, 4, 5] → 2 is in the correct place

Sort Left: none

Sort Right: [3, 8, 4, 5]

Pivot: 5

Partition → [3, 4, 5, 8]

Recursively sort left/right

Eventually → [2, 3, 4, 5, 8]




Algorithm      | Best Case     | Worst Case | Stable | In-Place | Notes
Bubble Sort    | O(n)          | O(n²)      | Yes    | Yes      | Simple but inefficient
Selection Sort | O(n²)         | O(n²)      | No     | Yes      | Always does same comparisons
Insertion Sort | O(n)          | O(n²)      | Yes    | Yes      | Good for small datasets
Merge Sort     | O(n log n)    | O(n log n) | Yes    | No       | Needs extra memory
Quick Sort     | O(n log n)    | O(n²)      | No     | Yes      | Fastest in practice
