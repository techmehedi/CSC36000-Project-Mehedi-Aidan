# CSC36000-Project-Mehedi-Aidan

## Project Title
Distributed Task Offloading and Learning with Adaptive Resource Allocation in Mobile Edge Computing

## Group Members
Mehedi Hasan  
Aidan Peña

## Course
CSC 36000 Modern Distributed Computing 

## Instructor
Professor Saptarashmi Bandyopadhyay

## Midterm Check In Date
November 26

---

## 1. Project Overview

The goal of this project is to improve the way AI or machine learning tasks are scheduled and executed in a distributed Mobile Edge Computing environment.

In real systems, devices such as phones, cameras, and IoT sensors send tasks to nearby edge servers. These servers have limited computing power and must decide how to distribute resources efficiently across many tasks.

This project compares three scheduling strategies:

1. Uniform scheduling  
2. Shortest Deadline First scheduling  
3. LARA style scheduling using adaptive resource allocation  

The main objective is to maximize the number of tasks completed before their deadlines while minimizing wasted computation.

---

## 2. What This Demo Shows

This Google Colab notebook runs a small simulation of an edge server that executes multiple machine learning tasks at the same time.

Each task has:
- A deadline  
- A difficulty level  
- A required accuracy threshold  
- A maximum processing speed  

The simulation runs over time and applies three different scheduling strategies to decide how much computing power each task receives.

The output includes:
- Which tasks finished successfully  
- Which tasks missed their deadline  
- The success rate of each scheduling method  

This demonstrates why an adaptive approach such as LARA outperforms basic methods.

---

## 3. Algorithms Implemented

### 3.1 Uniform Scheduler
This strategy splits computing power equally among all active tasks.  
It is used as a naive baseline.

### 3.2 Shortest Deadline First Scheduler
This strategy gives all computing power to the task that has the closest deadline.  
It is commonly used in real time systems.

### 3.3 LARA Style Scheduler
LARA stands for Learning with Adaptive Resource Allocation.

This strategy:
- Estimates how much work a task still needs
- Predicts if the task can finish before its deadline
- Allocates power to the most promising tasks
- Uses exploration first, then switches to exploitation

This is inspired by the LARA and CoRE-Learning research paper.

---

## 4. Code Structure

The notebook is organized into the following main components:

1. Task Model  
   Defines how a task behaves and how its learning curve works.

2. Progress Estimation  
   Uses discounted weighted least squares to estimate remaining work.

3. Scheduling Algorithms  
   Includes Uniform, Shortest Deadline First, and LARA style schedulers.

4. Simulation Engine  
   Advances time and runs each scheduling decision.

5. Results Output  
   Displays which tasks succeeded and the final success rate.

---

## 5. How To Run

1. Open the notebook in Google Colab.
2. Run every code cell from top to bottom.
3. Observe the printed results for each scheduling strategy.

No external setup, packages, or datasets are required.  
Everything runs with standard Python and NumPy.

---

## 6. Expected Results

You will see printed output for each strategy, including:

- When tasks complete
- When tasks miss their deadlines
- Final list of completed tasks
- Success rate as a percentage

Typical pattern:

- Uniform has the lowest success rate
- Shortest Deadline First performs better
- LARA style achieves the best performance

This directly supports the project goal.

---

## 7. Connection to Final Project

This demo is a simplified version of the full system.

For the final project, the following will be added:

- Multiple edge servers
- Network delay and bandwidth limits
- Energy usage tracking
- Latency measurements
- Performance graphs
- Scalability tests

This demo serves as the working foundation.

---

## 8. What Will Be Shown In Class

During the 4 minute presentation, we will demonstrate:

- The problem being solved
- The running simulation
- Performance comparison
- Why LARA works better

---

## 9. Contact

Mehedi Hasan  
City College of New York
CSC 36000

Aidan Peña  
City College of New York
