# DEPI Journey: Data Science Learning Path

A personal learning log for the DEPI (Digital Egypt Pioneers Initiative) Data Science track. The repository is organized to mirror the program's curriculum, with each topic folder holding a Jupyter notebook of worked examples, a Markdown quiz for self-assessment, and a Markdown summary distilling the key concepts covered — progressing from foundational data science concepts through Python, SQL, data analysis/visualization, and finally machine learning.

![Last Commit](https://img.shields.io/github/last-commit/OmarElzero/DEPI_Journey)
![Top Language](https://img.shields.io/github/languages/top/OmarElzero/DEPI_Journey)
![Repo Size](https://img.shields.io/github/repo-size/OmarElzero/DEPI_Journey)

## Features

- Nine curriculum modules, each with a worked-example notebook, a quiz, and a written summary
- Summaries covering: the data science methodology, popular tools, core Python, SQL and databases, data analysis with pandas/NumPy, data visualization, and machine learning fundamentals (supervised/unsupervised/reinforcement learning, the ML lifecycle from problem definition to deployment)
- Hands-on Jupyter notebooks reinforcing each topic with runnable code

## Tech Stack

- **Python 3**, **Jupyter Notebook**
- **pandas**, **NumPy** for data analysis
- **Matplotlib** / visualization libraries covered in the data visualization module
- **SQL** (covered in the databases module)
- **scikit-learn**-style machine learning concepts covered in the ML module

## Project Structure

| Path | Description |
|---|---|
| `Summarize/01-Introduction_to_Data_Science/` | Foundations and basic concepts |
| `Summarize/02-Data_Science_Methodology/` | Frameworks and approaches for solving data science problems |
| `Summarize/03-Tools_for_Data_Science/` | Overview of popular data science software and platforms |
| `Summarize/04-PythonForDataScience/` | Essential Python programming skills |
| `Summarize/05-PythonProjectForDataScience/` | Hands-on Python project work |
| `Summarize/06-DatabasesAndSQLForDataScience/` | Data management and SQL querying fundamentals |
| `Summarize/07-Data_Analysis_with_Python/` | Descriptive statistics, NumPy, pandas-based data analysis |
| `Summarize/08-Data_Visualization_with_Python/` | Techniques for visualizing data |
| `Summarize/09-Machine_Learning_with_Python/` | ML paradigms and the machine learning lifecycle |

Each module folder follows the same pattern: an `examples.ipynb` (or similarly named) notebook, a `quiz.md`, and a `summary.md`.

## Installation

```bash
git clone https://github.com/OmarElzero/DEPI_Journey.git
cd DEPI_Journey
pip install jupyter pandas numpy matplotlib
```

## Usage

Start with `Summarize/01-Introduction_to_Data_Science/` and progress sequentially, or jump to a specific topic:

```bash
jupyter notebook "Summarize/07-Data_Analysis_with_Python/examples.ipynb"
```

Review `summary.md` for concept notes and `quiz.md` in each folder to self-test understanding of that module.

## Demo

No live demo is available for this project.

---

**Author:** OmarElzero · [GitHub](https://github.com/OmarElzero)
Last updated: 2026-08-23
