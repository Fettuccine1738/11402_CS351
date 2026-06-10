# Project 0: Two Sum (Bootcamp)

## Introduction

This bootcamp project introduces the complete AI-assisted software development workflow through the implementation of the classic **Two Sum** problem from LeetCode. While the problem itself is relatively simple, the objective is to practice collaborating with AI throughout the engineering process, including requirements understanding, implementation, testing, code review, and documentation.

Students will implement and compare two different algorithmic approaches while applying modern software engineering practices such as automated testing, continuous integration, and containerized deployment.

**LeetCode Reference:** https://leetcode.com/problems/two-sum/

---

## Problem Statement

Given an array of integers `nums` and an integer `target`, return the indices of the two numbers whose sum equals `target`.

You may assume that:

* Each input contains exactly one valid solution.
* The same array element cannot be used twice.
* The answer may be returned in any order.

### Example

```cpp
nums = [2,7,11,15]
target = 9

Output: [0,1]
```

---

## Repository Information

**Repository Name:** `11402_CS351_Project0`

---

## Project Objectives

Upon completing this project, students should be able to:

* Apply AI-assisted workflows to software development tasks.
* Compare alternative algorithmic solutions to the same problem.
* Evaluate trade-offs between execution time and memory usage.
* Design and implement comprehensive unit tests.
* Build automated CI/CD pipelines.
* Package and distribute applications using Docker.

---

## Implementation Requirements

You are required to implement the following solutions:

### 1. TwoSumArray

A straightforward brute-force implementation using nested loops to search all possible pairs.

### 2. TwoSumHashTable

An optimized implementation using a hash table to achieve faster lookup performance.

Both implementations must produce identical results for all valid inputs.

---

## Testing Requirements

Create a comprehensive suite of automated unit tests that validates both implementations.

Your tests should include:

### Normal Cases

* Typical inputs with a valid solution.
* Arrays of varying sizes.

### Edge Cases

* Duplicate values.
* Negative numbers.
* Zero values.
* Solutions involving repeated numbers at different indices.

### Boundary Conditions

* Minimum valid input size.
* Large input arrays.
* Values near integer limits.

All tests should execute automatically through the project's test framework.

---

## Complexity Analysis

Document and justify the time and space complexity of each approach.

| Implementation  | Time Complexity | Space Complexity |
| --------------- | --------------- | ---------------- |
| TwoSumArray     | O(n²)           | O(1)             |
| TwoSumHashTable | O(n)            | O(n)             |

Your report should explain why these complexities arise and discuss the trade-offs between the two solutions.

---

## AI-Assisted Development Requirements

This project is intended to be completed using AI as a development partner.

Students should use AI tools to assist with:

* Requirements interpretation
* Solution design
* Code generation
* Debugging
* Test generation
* Documentation

However, students remain responsible for:

* Verifying correctness
* Understanding generated code
* Identifying potential defects
* Justifying design decisions

You should be prepared to explain and defend all submitted code.

---

## CI/CD Requirements

Configure a GitHub Actions workflow that automatically:

* Builds the project
* Executes all unit tests
* Reports failures

The workflow must run on:

* Every push
* Every pull request

---

## Docker Requirements

Containerize your solution using Docker.

Your submission must include:

* A `Dockerfile`
* Build instructions
* Test execution during the container build or validation process

The Docker image should provide a reproducible environment for building and testing the project.

---

## Deliverables

Your repository should contain:

* Source code for both implementations
* Unit tests
* Complexity analysis
* GitHub Actions workflow configuration
* Docker configuration
* Project documentation

The goal of this project is not simply to solve the Two Sum problem, but to practice a complete AI-assisted software engineering workflow from implementation to deployment.

