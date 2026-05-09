# Empirical Project: Data Science in Economics

## The Myth of the Hit Song Formula

**Module:** BEE2041 Data Science in Economics

This repository contains the full code, data, figures and website for the BEE2041 empirical project. The project investigates whether Spotify audio features can explain song popularity.

## Research question

Can Spotify audio features explain song popularity?

## Project summary

The project uses a public archived Spotify tracks dataset containing 114,000 tracks. After removing rows with missing core track information and dropping duplicate track IDs, the final analysis dataset contains 89,740 unique tracks.

Popular songs are defined as tracks at or above the 75th percentile of Spotify popularity scores. In this dataset, the popularity cutoff is 49, creating 22,520 popular tracks and 67,220 less-popular tracks.

The main finding is that Spotify audio features show some patterns, but they do not provide a simple hit-song formula. Popular songs are slightly more danceable and less instrumental on average, but the differences are modest. A logistic regression model achieves around 75% accuracy, but this is misleading because it identifies only about 1.4% of popular songs correctly. This suggests that audio features alone are weak predictors of popularity.

## Website output

The final data-driven blog website is published here:

https://tzening.github.io/bee2041-music-popularity-project/ 

## Repository structure

- `blog.ipynb`: Jupyter notebook containing the full analysis, cleaning, figures and model
- `index.html`: static data-driven blog post website
- `style.css`: website styling
- `data/raw/`: raw Spotify tracks dataset
- `data/cleaned/`: cleaned dataset exported from the notebook
- `figures/`: exported figures used in the blog post
- `requirements.txt`: Python packages required to run the notebook
- `.gitignore`: files ignored by Git, including macOS system files

## How to run the project

1. Clone or download this GitHub repository.
2. Install the required Python packages listed in `requirements.txt`.
3. Open `blog.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the notebook from top to bottom.
5. The notebook loads the raw dataset, cleans the data, creates the analysis dataset, exports figures to the `figures/` folder and runs the logistic regression model.
6. Open `index.html` to view the final website locally.

## Reproducibility

The analysis is reproducible from the files in this repository. The raw and cleaned datasets, notebook, exported figures and website files are included so the project can be rerun and checked.

The raw CSV file is stored in `data/raw/`, and the cleaned CSV file is stored in `data/cleaned/`. If GitHub cannot preview either CSV file because of its size, the files can still be downloaded from the repository or used directly when running `blog.ipynb`.

## Methods used

- Data loading and inspection
- Missing value and duplicate checks
- Data cleaning
- Feature transformation
- Grouped aggregation
- Data visualisation
- Correlation analysis
- Logistic regression classification
- Model evaluation using accuracy, recall and precision

## Tools used

- Python
- pandas
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook
- HTML and CSS
- Git and GitHub

## Limitations

The dataset is a public archived Spotify tracks dataset, not a live pull from Spotify's current API. Spotify popularity is a platform-based measure and the analysis is observational, so the results should not be interpreted as causal evidence.

The popular-versus-less-popular label also simplifies a continuous popularity score into two groups. This is useful for modelling, but it means the classification model should be interpreted as a simplified test of whether audio features can identify relatively popular tracks, not as a complete explanation of music success.
