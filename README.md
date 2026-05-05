LinkedIn Data Cleaning and Graph Analysis
1. Overview
This report outlines the process of cleaning LinkedIn connection data and applying graph theory
techniques to analyze the underlying social network. The data was extracted from multiple CSV files
where each file represents a user and their connections. Our goal is to build an adjacency list,
analyze connectivity, and visualize key insights.
2. Data Cleaning and Preparation
The cleaning process ensured all files were read correctly regardless of encoding. The key steps
include:
o
o
o
o
Auto-detecting and reading files with proper encoding.
Standardizing column names (e.g., converting to lowercase, trimming whitespace).
Dropping rows with missing or blank entries in essential columns like name and
company
Normalizing names to remove inconsistencies and building a uniform dataset.
Each user’s connections were collected by parsing their file and aggregating referenced connections.
Users without a personal file but mentioned in others were still included in the graph.
3. Graph Construction and Algorithms
•
Adjacency List Creation:
A dictionary structure stores users and their connections, forming a graph. This is exported
to a JSON file for further processing.
•
Node Count Calculation:
Each user's degree (number of connections) is computed and analyzed statistically (mean,
variance, etc.).
•
Random Walks:
Simulates how a person might traverse the network. Repeated steps are pruned to study
efficient paths.
Dominating Set:
A greedy algorithm identifies key nodes that can reach all others, helping to find influencers or
leaders in the network.
4. Visualizations
Various Python libraries were used (e.g., Matplotlib) to generate the following:
