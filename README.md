# NumPy Learning Repository

A collection of Jupyter notebooks demonstrating various NumPy operations and data analysis techniques. This repository contains hands-on exercises covering fundamental NumPy concepts, array operations, and real-world data analysis examples.

## Overview

This repository includes practical examples of:
- NumPy array creation and manipulation
- Data type handling and array reshaping
- Wine quality data analysis
- Optimization algorithms for team pairing
- Statistical analysis and data filtering

## Repository Structure

```
├── Notebook_ex00.ipynb    # Basic introduction
├── Notebook_ex01.ipynb    # Array creation with mixed data types
├── Notebook_ex02.ipynb    # Array initialization and reshaping
├── Notebook_ex03.ipynb    # [Additional NumPy operations]
├── Notebook_ex04.ipynb    # [Additional NumPy operations]
├── Notebook_ex05.ipynb    # [Additional NumPy operations]
├── Notebook_ex06.ipynb    # [Additional NumPy operations]
├── Notebook_ex07.ipynb    # [Additional NumPy operations]
├── Notebook_ex08.ipynb    # Wine quality data analysis
├── Notebook_ex09.ipynb    # Optimal team pairing algorithm
├── winequality-red.csv    # Red wine quality dataset
├── model_forecasts.txt    # Model prediction data for pairing analysis
└── requirements.txt       # Python dependencies
```

## 🚀 Getting Started

### Prerequisites

- Python 3.12+
- Jupyter Notebook or JupyterLab

### Installation

1. Clone this repository:
```bash
git clone https://github.com/moseeh/numpy-basics
cd numpy-basics
```

2. Create and activate a virtual environment:
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Linux/Mac:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Launch Jupyter:
```bash
jupyter notebook
```

## Notebook Contents

### Basic NumPy Operations
- **Notebook_ex01**: Demonstrates creating NumPy arrays with different Python data types using `dtype=object`
- **Notebook_ex02**: Shows array creation with `np.zeros()` and array reshaping operations

### Data Analysis Projects

#### Wine Quality Analysis (Notebook_ex08)
- Loads and analyzes red wine quality dataset (1,599 samples, 12 features)
- Performs statistical analysis including:
  - Data shape and memory usage analysis
  - Row selection and NaN handling
  - Alcohol content analysis and validation
  - pH statistics (min, max, percentiles, mean)
  - Quality correlation with sulphate levels
  - Comparison between best and worst quality wines

#### Team Pairing Optimization (Notebook_ex09)
- Implements optimization algorithm for optimal team pairing
- Uses model forecasts data (10x10 matrix with NaN values)
- Finds optimal pairing to minimize sum of squared differences
- Demonstrates use of itertools for combinations and permutations

## 🔧 Key Features

### NumPy Techniques Demonstrated
- Array creation and initialization
- Data type handling (`dtype=object`)
- Array reshaping and manipulation
- Statistical functions (`np.nanmean`, `np.nanpercentile`)
- Boolean indexing and masking
- File I/O with `np.genfromtxt` and `np.loadtxt`
- NaN handling and data cleaning

### Real-World Applications
- **Wine Quality Analysis**: Statistical analysis of wine characteristics
- **Team Optimization**: Algorithmic approach to optimal team pairing
- **Data Cleaning**: Handling missing values and data validation

## Dataset Information

### Wine Quality Dataset
- **File**: `winequality-red.csv`
- **Size**: 1,599 samples × 12 features
- **Features**: Physicochemical properties of red wine
- **Target**: Wine quality ratings

### Model Forecasts Data
- **File**: `model_forecasts.txt`
- **Format**: 10×10 matrix with comma-separated values
- **Contains**: NaN values requiring preprocessing
- **Usage**: Team pairing optimization algorithm

## Dependencies

Key packages used in this repository:

- `numpy==2.3.3` - Core numerical computing
- `jupyter==1.1.1` - Interactive notebook environment
- `jupyterlab==4.4.7` - Advanced notebook interface
- `matplotlib-inline==0.1.7` - Inline plotting support

See `requirements.txt` for complete dependency list.

## Learning Objectives

After working through these notebooks, you will understand:

1. **NumPy Fundamentals**
   - Array creation and manipulation
   - Data type handling
   - Array reshaping and indexing

2. **Data Analysis Skills**
   - Loading and preprocessing datasets
   - Statistical analysis and summary statistics
   - Boolean indexing and data filtering

3. **Algorithm Implementation**
   - Optimization algorithms
   - Combinatorial problem solving
   - Performance considerations

## Usage Examples

### Basic Array Operations
```python
import numpy as np

# Create array with mixed data types
arr = np.array([42, 3.14, "hello", [1,2,3]], dtype=object)

# Array reshaping
zeros_array = np.zeros(300)
reshaped = zeros_array.reshape(3, 100)
```

### Data Analysis
```python
# Load wine data
wine_data = np.genfromtxt('winequality-red.csv', delimiter=';', skip_header=1)

# Statistical analysis
alcohol_mean = np.nanmean(wine_data[:, 10])  # Alcohol column
pH_stats = np.nanpercentile(wine_data[:, 8], [25, 50, 75])  # pH quartiles
```

## Contributing

This is a learning repository. Feel free to:
- Add new NumPy examples
- Improve existing notebooks
- Add documentation or comments
- Suggest new datasets for analysis

## License

This project is for educational purposes. Dataset attributions:
- Wine quality data: UCI Machine Learning Repository

---

**Note**: This repository is designed for learning NumPy fundamentals through practical examples. Each notebook builds upon previous concepts while introducing new techniques for data manipulation and analysis.