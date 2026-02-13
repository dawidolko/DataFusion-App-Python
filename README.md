# DataFusion-App-Python 

> 🚀 **Powerful Data Analysis and Machine Learning GUI Application** - Build comprehensive data science platforms with Python, PySimpleGUI, and advanced analytics capabilities

## 📋 Description

Welcome to the **DataFusion App** repository! This user-friendly Python GUI application provides a comprehensive environment for real-world data analysis and machine learning. The application processes two distinct datasets: the UCI Adult Income dataset and the UCI Chronic Kidney Disease dataset, offering users powerful tools for data exploration, cleaning, transformation, statistical analysis, and predictive modeling.

Built with PySimpleGUI for an intuitive interface and leveraging industry-standard libraries like Pandas, Scikit-learn, Matplotlib, and Seaborn, this project demonstrates best practices in data science workflows, GUI development, and modular application architecture. Perfect for learning data analysis, machine learning algorithms, and building interactive data science applications.

## 📁 Repository Structure

```

DataFusion-App-Python/
├── 📁 database/ # Raw datasets
│ ├── 📊 adult.csv # UCI Adult Income Dataset
│ ├── 📊 chronic.csv # UCI Chronic Kidney Disease Dataset
│ └── 📖 README.md # Dataset documentation
├── 📁 docs/ # Project documentation
│ ├── 📝 description.docx # Detailed project description
│ ├── 📚 user-guide.pdf # User manual
│ └── 🔬 analysis-report.pdf # Analysis results
├── 📁 src/ # Application source code
│ ├── 🎯 main.py # GUI entry point and main application
│ ├── 📦 data_handler.py # Data loading and processing
│ ├── 📊 visualization.py # Plotting and visualization
│ ├── 🤖 ml_models.py # Machine learning algorithms
│ ├── 📈 statistics.py # Statistical analysis functions
│ ├── 🧹 preprocessing.py # Data cleaning and transformation
│ ├── 🖼️ assets/ # Application assets
│ │ └── screen-app.png # Application screenshot
│ └── 📋 requirements.txt # Python dependencies
├── 📄 LICENSE # MIT License
└── 📖 README.md # Project documentation

```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/dawidolko/DataFusion-App-Python.git
cd DataFusion-App-Python
```

### 2. Create Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Linux/macOS:
source venv/bin/activate

# On Windows:
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
# Install required packages
pip install -r src/requirements.txt
```

### 4. Start the Application

```bash
# Run the main application
python src/main.py
```

- The GUI application will launch automatically

## ⚙️ System Requirements

### **Essential Tools:**

- **Python** (version 3.8 or higher)
- **pip** package manager
- **Virtual environment** (venv or virtualenv)
- **Git** for version control

### **Development Environment:**

- **Code Editor** (VS Code, PyCharm, Sublime Text)
- **Python Debugger** for development
- **Jupyter Notebook** (optional, for data exploration)

### **Required Python Libraries:**

- **PySimpleGUI** - GUI framework
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Scipy** - Scientific computing

### **Recommended Tools:**

- **Git** for version control
- **Python Linter** (pylint, flake8)
- **Black** for code formatting
- **pytest** for testing

## ✨ Key Features

### **🖥️ Interactive GUI Interface**

- Simple and intuitive PySimpleGUI-based interface
- Perform complex data operations without coding
- User-friendly menu navigation
- Real-time operation feedback
- Progress indicators for long-running tasks

### **📊 Data Extraction and Transformation**

- Load multiple dataset formats (CSV, Excel, JSON)
- Handle missing data with multiple strategies
- Data normalization and standardization
- Encode categorical variables (one-hot, label encoding)
- Feature engineering and creation
- Data type conversion and validation

### **📈 Statistical Analysis**

- Calculate descriptive statistics (mean, median, mode, standard deviation)
- Quartiles and percentiles analysis
- Correlation matrix generation
- Distribution analysis and testing
- Hypothesis testing capabilities
- Outlier detection and handling

### **🤖 Machine Learning Algorithms**

#### **Classification Models:**

- **Decision Trees** - Rule-based classification
- **k-Nearest Neighbors (k-NN)** - Instance-based learning
- **Logistic Regression** - Probabilistic classification
- Model evaluation with accuracy, precision, recall, F1-score
- Confusion matrix visualization

#### **Clustering:**

- **K-Means Clustering** - Unsupervised grouping
- Elbow method for optimal cluster selection
- Cluster visualization and analysis
- Silhouette score evaluation

#### **Association Rules:**

- **Apriori Algorithm** - Pattern discovery
- Frequent itemset mining
- Rule generation with confidence and support
- Market basket analysis

### **📊 Data Visualization**

- **Histograms** - Distribution visualization
- **Scatter Plots** - Relationship exploration
- **Box Plots** - Statistical summary visualization
- **Heatmaps** - Correlation matrices
- **Bar Charts** - Categorical data comparison
- **Line Graphs** - Trend analysis
- Interactive plot customization
- Export visualizations to image files

### **🔧 Modular Architecture**

- Clean separation of concerns
- Easy to maintain and extend
- Independent module testing
- Reusable components
- Well-documented code

### **📚 Educational Focus**

- Ideal for learning data science workflows
- Real-world dataset examples
- Complete analysis pipelines
- Documented best practices
- Step-by-step guided processes

## 🛠️ Technologies Used

- **Python 3.8+** - Core programming language
- **PySimpleGUI** - GUI framework for desktop applications
- **Pandas** - Data manipulation and analysis library
- **NumPy** - Fundamental package for numerical computing
- **Scikit-learn** - Machine learning library
- **Matplotlib** - Comprehensive plotting library
- **Seaborn** - Statistical data visualization
- **Scipy** - Scientific computing tools

## 📚 Datasets

### **UCI Adult Income Dataset**

Demographic and employment data for income classification tasks:

- **Purpose:** Predict whether income exceeds $50K/year
- **Features:** Age, workclass, education, occupation, hours per week, etc.
- **Target:** Binary classification (>50K, <=50K)
- **Records:** ~48,000 entries

### **UCI Chronic Kidney Disease Dataset**

Medical parameters for diagnosing chronic kidney disease:

- **Purpose:** Binary classification of kidney disease presence
- **Features:** Blood pressure, specific gravity, albumin, blood glucose, etc.
- **Target:** CKD or not CKD
- **Records:** 400 medical cases

Both datasets are included in the `database/` directory with complete documentation.

## 📖 Usage Guide

### **1. Loading Data**

Launch the application and select "Load Dataset" from the menu. Choose between:

- Adult Income Dataset
- Chronic Kidney Disease Dataset
- Custom CSV file

### **2. Data Exploration**

Use the data exploration tools to:

- View dataset summary and statistics
- Check for missing values
- Explore data distributions
- Analyze feature correlations

### **3. Data Preprocessing**

Apply preprocessing operations:

- Handle missing values (drop, fill, interpolate)
- Normalize or standardize features
- Encode categorical variables
- Create new features

### **4. Statistical Analysis**

Generate statistical insights:

- Calculate descriptive statistics
- Create correlation matrices
- Perform distribution tests
- Identify outliers

### **5. Machine Learning**

Train and evaluate models:

- Select algorithm (Classification/Clustering/Association Rules)
- Configure model parameters
- Train on dataset
- Evaluate performance metrics
- Visualize results

### **6. Visualization**

Create insightful visualizations:

- Generate various plot types
- Customize appearance
- Export to image files
- Compare multiple features

## 🖼️ Application Screenshot

[<img src="src/assets/screen-app.png" width="80%" alt="DataFusion App Interface"/>](src/assets/screen-app.png)

## 🤝 Contributing

Contributions are highly welcomed! Here's how you can help:

- 🐛 **Report bugs** - Found an issue? Let us know!
- 💡 **Suggest improvements** - Have ideas for better features?
- 🔧 **Submit pull requests** - Share your enhancements and solutions
- 📖 **Improve documentation** - Help make the project clearer

Feel free to open issues or reach out through GitHub for any questions or suggestions.

## 👨‍💻 Author

Created by **[Dawid Olko](https://github.com/dawidolko)** - Part of the data science and machine learning series.

## 📄 License

This project is open source and available under the [MIT License](https://opensource.org/licenses/MIT).

---
