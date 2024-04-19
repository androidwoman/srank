# SibRank: SiBreNet Recommendation Framework

SibRank is a recommendation framework that leverages the SiBreNet (Structured Bipartite Network) algorithm. SiBreNet captures user preferences through a structured bipartite network, enabling the calculation of SRank values and the inference of personalized recommendations. This README provides an overview of the SibRank framework.

## Table of Contents
- [Introduction](#introduction)
- [Algorithm Overview](#algorithm-overview)
- [Dependencies](#dependencies)
- [Usage](#usage)
  - [1. SiBreNet Construction of Preference Data](#1-sibrenet-construction-of-preference-data)
  - [2. Calculating SRank of the Target User](#2-calculating-srank-of-the-target-user)
  - [3. Finding the Neighbors](#3-finding-the-neighbors)
  - [4. Ranking Inference](#4-ranking-inference)
  - [5. Top-k Recommendation](#5-top-k-recommendation)

## Introduction

SibRank is designed to provide personalized recommendations by constructing a structured bipartite network (SiBreNet) that captures user preferences. The framework includes steps for calculating SRank values, identifying neighbors, inferring rankings, and generating top-k recommendations.

## Algorithm Overview

### 1. SiBreNet Construction of Preference Data
   - **Input**: User preference data, including rankings and temporal sequences.
   - **Output**: Structured Bipartite Network (SiBreNet) capturing user preferences.

### 2. Calculating SRank of the Target User
   - **Input**: SiBreNet, target user (u).
   - **Output**: Positive and negative SRank values for nodes in SiBreNet.

### 3. Finding the Neighbors
   - **Input**: SRank values, SiBreNet.
   - **Output**: Neighbors of the target user based on SRank values.

### 4. Ranking Inference
   - **Input**: Neighbors, SiBreNet, target user.
   - **Output**: Estimated preference matrix for the target user.

### 5. Top-k Recommendation
   - **Input**: Estimated preference matrix, original ranking data.
   - **Output**: Top-k recommendations for the target user.

## Dependencies

- pandas
- numpy
- scipy
- networkx

Install the dependencies using the following command:
```bash
pip install pandas numpy scipy networkx
```

## Usage

### 1. SiBreNet Construction of Preference Data

Construct a structured bipartite network (SiBreNet) to capture user preferences, distinguishing between agreements and disagreements.

### 2. Calculating SRank of the Target User

Calculate positive and negative SRank values for nodes in SiBreNet, specifically for the target user.

### 3. Finding the Neighbors

Identify neighbors of the target user based on SRank values, considering users with similar preferences.

### 4. Ranking Inference

Infer the ranking preferences of the target user by considering the preferences of their neighbors in SiBreNet.

### 5. Top-k Recommendation

Provide top-k recommendations for the target user based on the inferred preferences.

Feel free to adjust parameters, file paths, or functions as needed for your specific use case. The framework aims to facilitate personalized recommendations by incorporating user preferences within a structured network.