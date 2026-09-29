# CS3810 Mini-Project 1: Search Algorithms for a Cleaning Robot

### Introduction to Artificial Intelligence Repository  
**Instructor:** Xin Wang

**Due Date:** 10/2/26  

---

## Project Overview

This repository contains the source code, experimental data, and final report for Mini-Project 1 in CS3810: Introduction to Artificial Intelligence. The goal of this project is to build and evaluate pathfinding planners for an automated grid-based cleaning robot (inspired by the Roomba). Given a known map, a starting position, and a set of dirty cells, the robot must find the cheapest sequence of actions to clean all dirty cells.

---

## Purpose & Goals

Early cleaning robots relied on semi-random movement to cover rooms, which was often slow and inefficient. Modern vacuum robots build maps and use state-space search algorithms to plan optimal routes.

The main objectives of this project are:
- Build a custom Vacuum World grid environment. 
- Implement and compare classical search algorithms (DFS, A*, and IDA*).
- Design, prove, and test admissible heuristics ($h_0$, $h_1$, $h_2$, and an optional $h_3$). 
- Run controlled experiments across various test grids to analyze search performance, path cost, and state-space growth.   


---

## Core Features

### Core Features & Environment Specification
Vacuum World Environment (VacuumWorld):
- Grid Setup: Rectangular grid with open spaces, obstacles (#), dirty cells (D), and a starting robot position (R).
- State Representation: A hashable tuple containing the robot's current position (row, col) and a frozenset of remaining dirty cells.
- Action Space: MOVE_UP, MOVE_DOWN, MOVE_LEFT, MOVE_RIGHT, and CLEAN.
- Deterministic Transitions: Actions are returned in a fixed order, ensuring fair comparisons and reproducible node counts.
  
---

