# Assessment Submission for Applied Statistics

gerry to work on this - but here is an idea of what it could look

This repository contains my submission for the module Applied Statistics.
The project is written in a single Jupyter notebook, in Python.
Everything needed to run the notebook is included in this repository.

## Quick Look
- You can click on [problems.ipynb] in this repository and GitHub will display it in static format.
- You can view and run the notebook in [Google Colab](https://colab.research.google.com/).
- You can view the notebook using [nbviewer] (https://nbviewer.org/) also.

## Running the Notebook
In order to run `problems.ipynb` you can follow these steps:

1. Clone the repository using [git](https://git-scm.com/).
2. Ensure you have [Python](https://www.python.org/) installed. An easy way to get Python is to use [uv](https://docs.astral.sh/uv/) or [Anaconda](https://www.anaconda.com/download).

## Dependencies

The notebook depends on the [numpy] (https://numpy.org/) package, the [matplotlib] (https://matplotlib.org/) package.

## About the Notebook

This notebopk looks at ...

## About the Author

 I am a mature student

# Applied Statistics Assessment

This repository contains the assessment for the Applied Statistics module. The analysis is implemented in a single Jupyter notebook using Python. All necessary code and data are included to ensure the analysis is fully reproducible upon cloning.

## Project Overview

This analysis applies fundamental statistical methods to the classic **Iris dataset** to investigate morphological differences between three flower species (*setosa*, *versicolor*, and *virginica*). The analysis is structured around four distinct problems:

1.  **Distribution Analysis:** Exploring the distribution of petal length using histograms and superimposed normal curves to assess normality.
2.  **Correlation Analysis:** Quantifying the relationship between petal length and petal width using Pearson correlation coefficients and scatter plots.
3.  **Hypothesis Testing (t-tests):** Comparing petal dimensions between species pairs using independent-samples t-tests.
4.  **Analysis of Variance (ANOVA):** Testing for overall differences between species while addressing the multiple comparisons problem.

## Repository Structure
.
├── problems.ipynb      # Main analysis notebook (Jupyter)
├── iris.csv            # Dataset (if applicable)
├── requirements.txt    # Python dependencies
└── README.md           # This file

*Note: If your dataset is loaded directly from a library (e.g., `seaborn` or `sklearn`), the `iris.csv` file may not be necessary. If you are using a raw CSV, ensure it is placed in the root directory as shown above.*

## Quick Look

You can view the notebook statically without installing anything:

*   **[View on GitHub](problems.ipynb):** GitHub renders Jupyter notebooks automatically.
*   **[View on nbviewer](https://nbviewer.org/):** Paste this repository URL into [nbviewer](https://nbviewer.org/) for a high-quality static render.
*   **[Run on Google Colab](https://colab.research.google.com/):** Upload `problems.ipynb` to Google Colab to execute it in the cloud without local setup.

## Running the Notebook Locally

To execute the analysis on your local machine, follow these steps:

### Prerequisites
Ensure you have **Python 3.9+** installed. If you do not have Python installed, the easiest methods are:
*   **[uv](https://docs.astral.sh/uv/):** A fast, modern Python package manager (recommended).
*   **[Anaconda](https://www.anaconda.com/download):** A distribution that includes Python and common data science tools.

### Installation & Execution

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
    cd YOUR_REPO_NAME
    ```

2.  **Set up the environment (choose one):**

    *Using `uv` (fastest):*
    ```bash
    uv venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    uv pip install -r requirements.txt
    ```

    *Using `pip` (standard):*
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Launch Jupyter:**
    ```bash
    jupyter notebook problems.ipynb
    ```
    or
    ```bash
    jupyter lab problems.ipynb
    ```

## Dependencies

The notebook relies on the following Python libraries, listed in `requirements.txt`:

| Library | Purpose |
| :--- | :--- |
| **[NumPy](https://numpy.org/)** | Numerical computing and array operations. |
| **[Pandas](https://pandas.pydata.org/)** | Data manipulation and loading the dataset. |
| **[Matplotlib](https://matplotlib.org/)** | Data visualization (histograms, scatter plots). |
| **[Seaborn](https://seaborn.pydata.org/)** | Statistical data visualization (optional, if used for enhanced plots). |
| **[SciPy](https://scipy.org/)** | Statistical functions (t-tests, ANOVA, Pearson correlation). |

*Note: While your original text mentioned only NumPy and Matplotlib, the analysis described (t-tests, ANOVA, correlation) requires **SciPy**. If you use Pandas for data handling, ensure it is listed as well.*

## Methodology Summary

### Problem 1: Exploring Petal Length
*   **Goal:** Investigate the distribution of `petal_length` across all flowers and within species.
*   **Approach:** Generate histograms for the full dataset and each species subset. Superimpose normal distribution curves using calculated means and standard deviations. Report descriptive statistics (mean, std) to visually assess normality.

### Problem 2: Correlation Between Petal Length and Petal Width
*   **Goal:** Quantify the linear relationship between `petal_length` and `petal_width`.
*   **Approach:** Calculate the Pearson correlation coefficient for the pooled dataset and separately per species. Visualize with scatter plots and regression lines to compare global vs. species-specific trends.

### Problem 3: Comparing Species Using t-Tests
*   **Goal:** Determine if significant differences exist in petal dimensions between species pairs.
*   **Approach:** Perform independent-samples t-tests (via `scipy.stats.ttest_ind`) for all species pairs (setosa vs. versicolor, setosa vs. virginica, versicolor vs. virginica) on both petal length and width. Evaluate results against a significance level of $\alpha = 0.05$.

### Problem 4: Comparing Species Using ANOVA
*   **Goal:** Test for differences among all three species simultaneously while controlling the family-wise error rate.
*   **Approach:** Conduct one-way ANOVA (via `scipy.stats.f_oneway`) for petal length and width. Discuss the limitations of pairwise t-testing (increased Type I error probability) and why ANOVA is statistically preferable for multi-group comparisons.

## Results & Conclusions

*(This section should contain a brief summary of your key findings after running the notebook. Example placeholders are provided below.)*

*   **Normality:** The distribution of petal length for the full dataset appears bimodal, violating the normality assumption. However, within individual species, distributions appear approximately normal.
*   **Correlation:** A strong positive correlation exists between petal length and width globally ($r \approx 0.96$), though correlations within species are weaker.
*   **Hypothesis Testing:** t-tests and ANOVA results indicate highly significant differences in petal dimensions across all species pairs ($p < 0.001$), confirming that petal morphology is a strong discriminator between iris species.

## About the Author

I am a mature student pursuing a **Higher Diploma in Data Analytics**. This project was completed as part of the **Applied Statistics** module. My background includes [briefly mention prior experience if relevant, e.g., transitioning from a previous career], and I am passionate about applying statistical rigor to solve practical problems.