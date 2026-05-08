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

## Data Processing Pipeline (April 13)
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
├── April 13 - DataWranglingDSML.ipynb                                          # Recent ipynb
├── Notes.txt                                                                   # Literature review spreadsheet link
├── Spring26 - DS_MLCourseProjectPaper-Mehak-Julie.pdf                          # Compiled paper
├── Spring26 - DS_MLCourseProjectPaper-Mehak-Julie.pdf                          # Compiled paper
├── UniquePPs.zip                                                               # .zip Raw GraphML dataset
├── all_companies_metrics.csv                                                   # .csv file
├── Data Collection, Data Wrangling, and Visualization.ipynb                    # .ipynb notebook (EDA & preprocessing)
├── figures/                                                                    # Generated visualizations (Figures 1–7)
├── April13figures/                                                             # Answer to RQ1 and RQ2
├── Mehak_Julie _Milestone II Presentation - DS&ML.pptx                         # Slides
├── (April29)figures/                                                           # Generated visualizations Final Milestone
├── TheFinal Presentation-DS&ML.pptx                                            # Slides
├── (April_29)Mehak_Julie_Privacy_Policy_KG.ipynb                               # .ipynb notebook (Final)
├── (April_29)Mehak_Julie_Privacy_Policy_KG.pdf                                 # pdf of .ipynb notebook (Final)
├── Spring26 - DS&MLCourseProject-Mehak-Julie (April 29)                        #Compiled paper
├── (May7)figures/                                                              # Generated visualizations Final Milestone
├── Spring26 - DS&MLCourseProject-Mehak-Julie (May7)                            #Compiled paper
└── README.md                                                                   # Project documentation
```

## Final Milestone
This project analyzed privacy policies from 184 S&P 500 companies across three sectors, Healthcare, IT, and Financial, using knowledge graph analytics. Each company's privacy policy was represented as a GraphML file containing ACTOR nodes, representing entities that collect data, and DATA nodes, representing the types of data collected, connected by COLLECT and SUBSUM edges. We built a unified knowledge graph combining all 184 companies into one structure, linking companies to sectors, data types to regulatory frameworks, and actors to their collection relationships. Using this graph, we applied graph algorithms including BFS, DFS, shortest path, and all-paths analysis to trace how data flows through the graph and identify structural patterns. We then ran centrality analysis, PageRank, in-degree, and betweenness, to identify which nodes are most structurally influential across the entire corpus. Finally, we matched every collected data type against official GDPR, CCPA, and HIPAA regulatory vocabularies to measure compliance exposure per sector. Our two research questions drove the analysis: RQ1 asked what connections and compliance patterns exist across sectors, and RQ2 asked what data types, third-party actors, and collection patterns are characteristic within each sector. The results revealed a two-tier structure across all three sectors: a universal baseline of digital identifiers collected by virtually every company, and a sector-specific sensitive data tier that diverges sharply by industry. The most significant finding was that HIPAA exposure extends well beyond Healthcare — 77% of IT companies and 81% of Financial companies collect data matching HIPAA's 18 Safe Harbor identifiers, revealing compliance obligations that their sector classification alone would not predict.

## Team Members
Mehakpreet Kaur

Julie Allen

## Last Updated
May 7, 2026

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
