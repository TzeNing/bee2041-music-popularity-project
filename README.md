# BEE2041 Music Popularity Project

This project investigates whether Spotify audio features can explain song popularity.

## Research question

Can Spotify audio features explain song popularity?

## Project summary

The project uses a public archived Spotify tracks dataset containing 114,000 tracks. After cleaning and removing duplicate tracks, the final analysis dataset contains 89,740 unique tracks. Popular songs are defined as tracks at or above the 75th percentile of Spotify popularity scores.

The main finding is that Spotify audio features show some patterns, but they do not provide a simple hit-song formula. Popular songs are slightly more danceable and less instrumental on average, but the differences are modest. A logistic regression model performs poorly at identifying popular songs, suggesting that audio features alone are weak predictors of popularity.

## Repository structure

- `blog.ipynb`: Jupyter notebook containing the full analysis
- `index.html`: static blog post website
- `style.css`: website styling
- `data/`: raw and cleaned datasets
- `figures/`: exported figures used in the blog post
- `requirements.txt`: Python packages required for the project

## Website output

The final data-driven blog website is published here:

[Insert GitHub Pages link here]

If the website link is not yet live, the blog can also be viewed by opening `index.html` from the project folder.

## How to run the project

1. Clone or download this GitHub repository.
2. Install the required Python packages listed in `requirements.txt`.
3. Open `blog.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the notebook from top to bottom.
5. The notebook loads the raw dataset, cleans the data, creates the analysis dataset, exports figures to the `figures/` folder and runs the logistic regression model.
6. Open `index.html` to view the final website locally.

## Reproducibility

The analysis is reproducible from the files in this repository. The raw and cleaned datasets, notebook, exported figures and website files are included so the project can be rerun and checked.

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

## Limitations

The dataset is a public archived Spotify tracks dataset, not a live pull from Spotify's current API. Spotify popularity is a platform-based measure and the analysis is observational, so the results should not be interpreted as causal evidence.
