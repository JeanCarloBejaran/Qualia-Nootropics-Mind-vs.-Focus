# Qualia Nootropics: Mind vs. Focus Ingredient Analysis

Nootropic ingredients comparison of Qualia Mind vs. Qualia Focus: 
Two nootropic stacks created by neurohacker.
Website: https://neurohacker.com/

# Problem 
  What are the effects of switching to Qualia Focus?

### Framing the problem as a mathematical question:
  How similar are Qualia Mind and Qualia Focus? 
  What are the differences down to the ingredient level?

## Methodology

### 1. Data Acquisition
- **Data Sources**: Extracted ingredient information from the official Qualia Mind and Qualia Focus product pages.
- **Data Retrieval**: Utilized the `requests` library with custom headers to bypass HTTP 403 errors and mimic browser requests.
- **Parsing**: Employed `pandas.read_html` to scrape and parse ingredient tables from the retrieved HTML content.

### 2. Data Cleaning and Preparation
- **DataFrame Construction**: Created separate pandas DataFrames for Qualia Mind and Qualia Focus ingredients.
- **Column Renaming**: Standardized column names for consistency across datasets.
- **Data Cleaning**:
  - Removed irrelevant rows and columns to focus on essential ingredient data.
  - Extracted and converted ingredient amounts from strings to integer values representing milligrams per serving.
  - Generated merge keys based on truncated ingredient names to facilitate accurate merging.
- **Data Merging**: Merged the Mind and Focus DataFrames on the generated keys to compare ingredient quantities side-by-side.
- **Handling Missing Data**: Filled missing ingredient quantities in Qualia Focus with zeroes to indicate absence.

### 3. Data Analysis
- **Identifying Differences**: Filtered out ingredients with identical quantities in both formulations to highlight key differences.
- **Effect Annotation**: Manually added effect descriptions for each differing ingredient based on information from the Neurohacker website.
- **Percentage Change Calculation**: Calculated the percentage change in ingredient amounts from Mind to Focus to quantify differences.
- **Visualization**: Prepared for visual analysis using `matplotlib`, `seaborn`, and `plotly.express` to create informative plots illustrating ingredient variations.

## Technologies Used

- **Programming Language**: Python 3.x
- **Libraries**:
  - [Pandas](https://pandas.pydata.org/) for data manipulation and analysis
  - [Requests](https://requests.readthedocs.io/) for handling HTTP requests
  - [Matplotlib](https://matplotlib.org/) for creating static visualizations
  - [Seaborn](https://seaborn.pydata.org/) for statistical data visualization
  - [Plotly Express](https://plotly.com/python/plotly-express/) for interactive visualizations
- **Development Environment**:
  - [Jupyter Notebook](https://jupyter.org/) for interactive coding and documentation
  - [Google Colab](https://colab.research.google.com/) for cloud-based notebook execution
- **Version Control**:
  - [Git](https://git-scm.com/) for version tracking
  - [GitHub](https://github.com/) for repository hosting
- **Potential Future Tools**:
  - [NLTK](https://www.nltk.org/) for natural language processing tasks

## Getting Started

To replicate the analysis:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/JeanCarloBejaran/Qualia-Nootropics-Mind-vs.-Focus.git


# Conclusion
  Qualia Focus and Qualia Mind are very similar. From 28 total ingredients, 4 were completely removed and 5 were changed in total quantities.
  
  So far, based on the data, Qualia Mind does appear to promote overall brain health for short and long-term mental well-being. With the ingredient changes in Focus, the trade-off appears to be on removing the dimension of long-term wholistic mental health and focusing on a "thinking fast on your feet" approach: increasing attention and working memory.

If transitioning, you can expect a decline in long term health factors such as neuroprotective effects, aging memory decline prevention, executive function and stress reduction. 

*Notes: 
The data we used is no longer accessible from the maker's website.


