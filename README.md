# DataFusion

> 📊 **A CSV workbench that runs on the desktop** — load, clean, encode, scale and plot a dataset without writing a line of pandas

**DataFusion** is a desktop application for the part of data science that comes before the model: opening a file, finding out what is wrong with it, and fixing it. Load a CSV or one of the two bundled UCI datasets, read the statistics, fill or drop the missing values, encode the categorical columns, scale the numeric ones, and draw the chart that shows whether any of it worked.

Every transformation happens on a working copy, and one button puts the original data back — so exploring destructively is safe.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![PySimpleGUI](https://img.shields.io/badge/PySimpleGUI-desktop-5A9FD4)
![pandas](https://img.shields.io/badge/pandas-2.0%2B-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3%2B-F7931E?logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8%2B-11557C?logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🎯 Key Features

- **Undo is a first-class button** — the original frame is kept beside the working one, so any cleaning step can be reversed without reloading the file.
- **Descriptive statistics on demand** — count, mean, spread, plus skewness and kurtosis from SciPy, which are the two that actually tell you whether a distribution will behave.
- **Both correlation matrices, side by side** — Pearson and Spearman together, because a monotonic relationship that is not linear is exactly what one of them hides.
- **Missing values handled by strategy, not by hand** — pick a strategy and it is applied to the frame; duplicates are removed the same way.
- **Three encodings for categorical columns** — one-hot, binary and target encoding, chosen per column rather than applied blindly to everything.
- **Scaling on selected columns** — standard or min-max, applied to the columns you choose, so an identifier column is not scaled along with the measurements.
- **Five chart types, each configurable** — histogram, box plot, bar chart, line plot and pie chart, drawn with Matplotlib into the window and saveable as an image.
- **Sub-tables by row and column index** — extract or exclude a slice and keep working on it.
- **Two datasets included** — UCI Adult and Chronic Kidney Disease, ready to open without hunting for a file.

---

## 🖼️ Screenshots

| The main view                                       | Descriptive statistics                               |
| --------------------------------------------------- | ---------------------------------------------------- |
| ![The DataFusion main window with a loaded dataset](src/assets/main_view.png) | ![Descriptive statistics for the loaded frame](src/assets/data_stats.png) |

| Cleaning and transformation                          | Correlation matrices                                 |
| ---------------------------------------------------- | ---------------------------------------------------- |
| ![Missing values, duplicates and encoding controls](src/assets/data_cleaning_transformation.png) | ![Pearson and Spearman side by side](src/assets/correlation_results.png) |

| Charts                                               | Scaling results                                      |
| ---------------------------------------------------- | ---------------------------------------------------- |
| ![Histogram, box plot and the other chart types](src/assets/data_visualizations.png) | ![Columns after standard and min-max scaling](src/assets/scaling_results.png) |

---

## 📚 Bundled Datasets

| Dataset                      | Rows   | What it is                                           |
| ---------------------------- | ------ | ---------------------------------------------------- |
| **UCI Adult**                | 48 842 | Census data; the classic income-prediction benchmark. |
| **Chronic Kidney Disease**   | 400    | Clinical measurements in ARFF, with many missing values — which is the point of loading it. |

Both live in `database/`, with their original `.names` and `.info` files, so the column meanings are not lost.

---

## 🛠️ Technology Stack

| Technology       | Version | Role                                                        |
| ---------------- | ------- | ----------------------------------------------------------- |
| **PySimpleGUI**  | —       | The window, tabs, tables and dialogs.                        |
| **pandas**       | 2.0+    | The data frame everything operates on.                       |
| **NumPy**        | —       | Numeric operations underneath.                               |
| **scikit-learn** | 1.3+    | `StandardScaler` and `MinMaxScaler`.                         |
| **SciPy**        | —       | Skewness and kurtosis.                                       |
| **Matplotlib**   | 3.8+    | Charts, embedded in the window through `FigureCanvasTkAgg`.  |
| **Pillow**       | —       | Icons and image export.                                      |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or newer
- Tkinter available in the interpreter (it ships with most CPython builds)

### 1. Clone the repository

```bash
git clone https://github.com/dawidolko/DataFusion-App-Python.git
cd DataFusion-App-Python
```

### 2. Install dependencies

```bash
pip install PySimpleGUI pandas numpy scikit-learn scipy matplotlib pillow
```

### 3. Run

```bash
python src/main.py
```

The window opens with a start screen; **Go to data** loads either a bundled dataset or a CSV of your own.

---

## 📁 Project Structure

```
DataFusion-App-Python/
├── src/
│   ├── main.py             # the whole application: window, tabs, transformations, charts
│   └── assets/             # icons and the screenshots used above
├── database/
│   ├── adult/              # UCI Adult: data, test split, column names
│   └── chronic/            # Chronic Kidney Disease in ARFF, with its info file
└── docs/                   # documentation, task descriptions
```

---

## 📄 License

MIT © [Dawid Olko](https://dawidolko.pl)
