# Knowledge Graph-Based Comparative Privacy Policy Analysis
## Project Overview

This research project develops a knowledge graph analytics and machine learning framework for comparative privacy policy analysis across Financial, Healthcare, and IT sectors.

The dataset consists of graph-based representations of privacy policies from ~180+ Fortune 500 companies, generated using the PoliGrapher pipeline (Cui et al., 2023). Privacy policies were collected from company websites, converted to HTML, and transformed into structured GraphML knowledge graphs, enabling quantitative analysis of policy structure, complexity, and data-sharing behavior.

The project integrates:

Graph-based feature extraction
Data wrangling and preprocessing
Exploratory data analysis (EDA)
Machine learning-ready feature engineering

to identify patterns in privacy practices and detect deviations from regulatory norms.

## Research Questions
RQ1: What are Privacy Policy related connections across IT, Healthcare, and Financial Services with regulatory compliance impact and compliance violations, and how do the sectors compare?

RQ2: What are Privacy Policy related connections within the sectors of Information Technology, Healthcare, and Financial Services?


## Dataset Description
Source: Constructed using the PoliGrapher pipeline (Cui et al., 2023)

Input: Public privacy policies from Fortune 500 companies

Format: GraphML (knowledge graphs)

Scope: 184 companies across 3 sectors:
Financial
Healthcare
IT

Each graph encodes:

Nodes: data types, actors (entities), and policy elements
Edges: relationships (e.g., data collection, sharing, processing)

## Data Processing Pipeline
### Part A: Data Acquisition & Description
Dataset constructed from publicly available privacy policies
Graph-based representation using PoliGrapher
Comprehensive data dictionary and feature documentation
### Part B: Data Wrangling & Preprocessing
Missing value analysis and structural validation (e.g., empty graphs removed)
Data type conversion and categorical encoding
Outlier detection using:
IQR method
Z-score method
Feature engineering:
complexity_ratio
actor_ratio
data_ratio
complexity_tier
Feature scaling using StandardScaler
Final cleaned dataset exported for modeling
### Part C: Exploratory Data Analysis (EDA)
Distribution analysis of key graph metrics
Correlation heatmap of structural features
Sector-based comparisons (bar charts, pie charts, boxplots)
Scatter plots analyzing policy complexity relationships
Identification of outliers and high-complexity companies

 
## Repository Structure
```
├── main.tex                                                                    # Main LaTeX document
├── references.bib                                                              # Bibliography file
├── DS_MLCourseProjectPaper__March_10__2026_.pdf                                # Compiled paper
├── UniquePPs.zip                                                               # .zip Raw GraphML dataset
├── all_companies_metrics.csv                                                   # .csv file
├── Data Collection, Data Wrangling, and Visualization.ipynb                    # .ipynb notebook (EDA & preprocessing)
├── figures/                                                                    # Generated visualizations (Figures 1–7)
├── Notes.txt                                                                   # Literature review spreadsheet link
└── README.md                                                                   # Project documentation
```
## Team Members
Mehakpreet Kaur

Julie Allen

## Last Updated
April 13, 2026

## Running the Project
Google Colab (Recommended)

Download and extract UniquePPs.zip

Open the .ipynb notebook

Run cells sequentially to:

Load GraphML files

Generate features

Perform preprocessing

Produce visualizations

## LaTeX Paper Compilation

Option 1: Overleaf (Recommended)

Go to Overleaf

Import this repository from GitHub

The document will compile automatically
