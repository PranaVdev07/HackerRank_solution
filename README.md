
🧠 HackerRank Solutions: 3rd Semester Portfolio

Course: Portfolio Building (B25CS0311) Activity 8: HackerRank Algorithmic Problem-Solving & Portfolio Integration

HackerRank Show Image Show Image Show Image

👤 Student Details
Field	Details
Name	Pranav Pandey
Roll No.	R25EJ104
Branch	B.Tech CSIT
Section	B
Semester	3rd
HackerRank	pranavpandey260
🎯 Activity Overview

This repository contains my solutions to the 5 mandatory HackerRank problems from the 3rd-semester Portfolio Building studio activity. All solutions are written in Python 3. The goals are to demonstrate:

Core problem-solving using linear data structures and dynamic arrays
Time and space complexity analysis for every solution
A clean, documented repository linked to a public HackerRank profile
A Problem Solving badge on HackerRank (see Badge Status)

Day-by-day work is logged in PROGRESS.md.

📋 Problem Set & Complexity Analysis
#	Problem	Category	Key Concept	Time	Space	Status
1	Diagonal Difference	2D Arrays / Matrices	Matrix traversal, primary & secondary diagonal sums	O(N)	O(1)	✅ Accepted
2	Dynamic Array	Data Structures / Vectors	2D nested sequence manipulation, bitwise XOR	O(N + Q)	O(N)	✅ Accepted
3	Time Conversion	Strings & Logic	12-hour AM/PM to 24-hour military time	O(1)	O(1)	✅ Accepted
4	Compare the Triplets	Basic Implementation	Element-wise comparison & score tracking	O(1)	O(1)	✅ Accepted
5	Sparse Arrays	Hash Maps / Strings	Frequency mapping, efficient string matching	O(N + Q)	O(N)	✅ Accepted

Note: For Diagonal Difference, N is the matrix dimension (N × N). For Dynamic Array and Sparse Arrays, N is the number of elements/strings and Q is the number of queries.

💡 Approach Summary
1. Diagonal Difference

Traverse the matrix once using a single index i, adding arr[i][i] to the primary sum and arr[i][n-1-i] to the secondary sum. The answer is the absolute difference of the two.

2. Dynamic Array

Maintain a list of n empty sequences and a variable lastAnswer. For each query, compute the index (x ^ lastAnswer) % n. Type 1 appends y to that sequence; Type 2 reads the element at y % size and stores it in lastAnswer.

3. Time Conversion

Parse the hour and the AM/PM suffix. Handle the edge cases: 12:xx:xxAM becomes 00:xx:xx and 12:xx:xxPM stays 12:xx:xx. For other PM times, add 12 to the hour.

4. Compare the Triplets

Compare a[i] and b[i] for each of the three positions. Award a point to Alice if a[i] > b[i], to Bob if a[i] < b[i], and none on a tie.

5. Sparse Arrays

Build a hash map of string → frequency in a single pass. Each query is then answered in O(1) with a dictionary lookup instead of rescanning the list.

✅ Accepted Submissions
Problem	Result	Score
Diagonal Difference	Accepted (Python 3)	10 / 10
Dynamic Array	Accepted (Python 3)	15 / 15
Time Conversion	Accepted (Python 3)	100 / 100
Compare the Triplets	Accepted (Python 3)	10 / 10
Sparse Arrays	Accepted (Python 3)	25 / 25
1. Diagonal Difference
<img src="./screenshots/accepted/01-diagonal-difference.png" alt="Diagonal Difference - Accepted" width="800">
2. Dynamic Array
<img src="./screenshots/accepted/02-dynamic-array.png" alt="Dynamic Array - Accepted" width="800">
3. Time Conversion
<img src="./screenshots/accepted/03-time-conversion.png" alt="Time Conversion - Accepted" width="800">
4. Compare the Triplets
<img src="./screenshots/accepted/04-compare-the-triplets.png" alt="Compare the Triplets - Accepted" width="800">
5. Sparse Arrays
<img src="./screenshots/accepted/05-sparse-arrays.png" alt="Sparse Arrays - Accepted" width="800">
🏅 HackerRank Badge Status
<img src="./screenshots/badges/problem-solving-badge.png" alt="HackerRank Problem Solving badge" width="600">
Item	Status
Badge earned	Problem Solving: 1 Star ⭐
Problem Solving points	60 / 100 (at the time of the last screenshot)
Points to 2nd star	40
Course target	3-Star badge (in progress; see PROGRESS.md)
Public profile	https://www.hackerrank.com/profile/pranavpandey260
📁 Repository Structure
hackerRank_solution/
│
├── 01-Diagonal-Difference/
│   └── solution.py
├── 02-Dynamic-Array/
│   └── solution.py
├── 03-Time-Conversion/
│   └── solution.py
├── 04-Compare-the-Triplets/
│   └── solution.py
├── 05-Sparse-Arrays/
│   └── solution.py
│
├── screenshots/
│   ├── accepted/        # 5 "Accepted" submission screenshots
│   └── badges/          # HackerRank badge screenshot
│
├── PROGRESS.md          # Activity log & status tracker
└── README.md
🔗 Important Links
🔹 HackerRank Profile: https://www.hackerrank.com/profile/pranavpandey260
📝 Reflection: Algorithmic Optimization

Working through these problems showed me how much the choice of data structure matters. Sparse Arrays is a good example: scanning the whole list for every query is O(N × Q), while building a frequency map once brings it down to O(N + Q). Diagonal Difference taught me to look for the single-pass solution, since both diagonals can be summed in one loop with constant extra space. Dynamic Array reinforced how bitwise XOR and modulo can be combined to index into nested structures safely; my first submission returned a wrong answer, which taught me to trace the query logic on the sample input before submitting. Even the simplest problems, Time Conversion and Compare the Triplets, were a reminder that edge cases (12 AM / 12 PM, ties) cause most failed test cases, not the core logic.

🚀 How to Run
bash
cd 01-Diagonal-Difference
python solution.py

Each solution reads from standard input in the same format as the HackerRank problem statement.
