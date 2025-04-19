# AI-Enhanced Exploratory Data Analysis (EDA) Tools

This repository contains tutorials, code examples, and resources for performing exploratory data analysis using modern AI-powered tools. These tools can significantly speed up your data analysis workflow and provide insights that might be difficult to discover manually.

## 📋 Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Available Tools](#available-tools)
- [Getting Started](#getting-started)
- [Advanced Usage](#advanced-usage)
- [Contributing](#contributing)
- [License](#license)

## 🚀 Introduction

Exploratory Data Analysis (EDA) is a critical step in any data science project, allowing analysts to understand data characteristics, identify patterns, and detect anomalies. AI-enhanced EDA tools leverage machine learning and natural language processing to automate and augment this process, making it more efficient and insightful.

This repository provides resources for both beginners and advanced users to harness the power of these AI tools.

## 📦 Installation

### Prerequisites

- Python 3.7+
- pip (Python package manager)

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ai-enhanced-eda.git
   cd ai-enhanced-eda
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install basic dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install specific tools as needed:
   ```bash
   # For PyGWalker
   pip install pygwalker

   # For Pandas-AI
   pip install pandasai

   # For AutoViz
   pip install autoviz

   # For DataPrep
   pip install dataprep

   # For SweetViz
   pip install sweetviz

   # For D-Tale
   pip install dtale
   ```

## 🧰 Available Tools

### 1. PyGWalker
[PyGWalker](https://github.com/Kanaries/pygwalker) transforms your pandas DataFrame into an interactive Tableau-like interface directly in Jupyter notebooks.

**Key Features:**
- Drag-and-drop interface for visualization
- Multiple chart types
- Data filtering and transformation
- Export capabilities

### 2. Pandas-AI
[Pandas-AI](https://github.com/gventuri/pandas-ai) allows you to explore data using natural language queries.

**Key Features:**
- Query data using natural language
- Generate visualizations with text commands
- Perform complex analysis without coding
- Requires OpenAI API key

### 3. AutoViz
[AutoViz](https://github.com/AutoViML/AutoViz) automatically visualizes datasets with minimal code.

**Key Features:**
- Automatic visualization selection
- Feature relationship exploration
- Target variable-based analysis
- Minimal configuration required

### 4. DataPrep
[DataPrep](https://dataprep.ai/) simplifies data preparation and exploratory analysis.

**Key Features:**
- Comprehensive EDA reports
- Data cleaning capabilities
- Performance optimization for large datasets
- API for integration into workflows

### 5. SweetViz
[SweetViz](https://github.com/fbdesignpro/sweetviz) provides beautiful visualizations for EDA and data comparison.

**Key Features:**
- High-density visualizations
- Dataset comparison
- Target analysis
- Feature associations

### 6. D-Tale
[D-Tale](https://github.com/man-group/dtale) offers an interactive interface for pandas DataFrame analysis.

**Key Features:**
- Web-based interface
- Correlation analysis
- Charting and visualization
- Statistical testing

## 🏁 Getting Started

### Basic Example

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load your dataset
df = pd.read_csv('your_dataset.csv')

# Basic pandas EDA
print(df.info())
print(df.describe())

# Missing values check
print(df.isnull().sum())

# Try PyGWalker for interactive visualization
import pygwalker as pyg
walker = pyg.walk(df)  # Opens interactive interface in Jupyter notebook
```

### Using Pandas-AI

```python
from pandasai import PandasAI
from pandasai.llm.openai import OpenAI

# Set up the LLM
llm = OpenAI(api_token="your-openai-api-key")

# Initialize PandasAI with the LLM
pandas_ai = PandasAI(llm)

# Ask questions about your data
response = pandas_ai(df, "What's the correlation between column A and column B?")
print(response)

# Generate a visualization
response = pandas_ai(df, "Create a scatter plot of A vs B colored by C")
```

### Creating Automated Reports

```python
# Using DataPrep
from dataprep.eda import create_report
report = create_report(df, title='My Dataset Analysis')
report.show_browser()

# Using SweetViz
import sweetviz as sv
report = sv.analyze(df, target_feat='target_column')
report.show_html('sweetviz_report.html')
```

## 🔍 Advanced Usage

### Comprehensive Workflow Example

The file `ai_eda_examples.py` in this repository demonstrates a comprehensive workflow that combines multiple AI-enhanced EDA tools:

```bash
python ai_eda_examples.py
```

This script allows you to:
- Perform basic EDA with pandas
- Generate automated reports with DataPrep and SweetViz
- Explore data using natural language with Pandas-AI
- Create interactive visualizations with PyGWalker
- Run automated visualization with AutoViz
- Launch interactive analysis with D-Tale

### Integration Strategies

For the most effective use of these tools, consider this workflow:

1. **Initial Profiling**: Use DataPrep or SweetViz for a quick overview
2. **Question Formulation**: Based on initial findings, form questions
3. **Natural Language Exploration**: Use Pandas-AI to answer specific questions
4. **Interactive Deep Dive**: Use PyGWalker or D-Tale for detailed investigation
5. **Documentation**: Export findings as reports or visualizations

## 📈 Performance Considerations

- Most tools work well for datasets up to a few hundred thousand rows
- For larger datasets:
  - Sample your data first for initial exploration
  - Use tools with efficient data handling (DataPrep, D-Tale)
  - Consider chunking your analysis by columns or subsets
  - For very large datasets, consider distributed processing frameworks

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add some amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

<div align="center">


## 🌟 Support This Project
**Follow me on GitHub**: [![GitHub Follow](https://img.shields.io/github/followers/Harrypatria?style=social)](https://github.com/Harrypatria?tab=followers)
**Star this repository**: [![GitHub Star](https://img.shields.io/github/stars/Harrypatria/SQLite_Advanced_Tutorial_Google_Colab?style=social)](https://github.com/Harrypatria/SQLite_Advanced_Tutorial_Google_Colab/stargazers)
**Connect on LinkedIn**: [![LinkedIn Follow](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harry-patria/)

Click the buttons above to show your support!

</div>



## 🙏 Acknowledgments

- The creators and maintainers of all the tools mentioned
- The data science community for continued innovation in EDA techniques
