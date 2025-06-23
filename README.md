# Regression Models

A Jupyter notebook implementing Linear, Quadratic, and Cubic regression models with visualization and performance comparison.

## Features

- Linear Regression (Degree 1)
- Polynomial Regression (Degree 2 & 3)
- R² Score and SSE calculation
- Training and test set visualizations

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/Regression-Models.git
cd Regression-Models
```

2. Install dependencies
```bash
pip install numpy matplotlib pandas scikit-learn jupyter
```

3. Start Jupyter Notebook
```bash
jupyter notebook
```

## Usage

1. Place your dataset as `Data.csv` in the project folder
2. Open `Regression_models.ipynb`
3. Run all cells or execute step by step

### Dataset Format
```csv
feature1,feature2,target
1.2,2.3,5.1
2.1,3.4,7.2
```

## Results

Each model outputs:
- **R² Score**: Model accuracy (higher = better)
- **SSE**: Sum of squared errors (lower = better)
- **Plots**: Red dots (data) + Blue line (regression)

## Files

- `Regression_models.ipynb` - Main notebook
- `Data.csv` - Your dataset

## Contributing

1. Fork the repo
2. Create a feature branch
3. Make your changes
4. Submit a pull request

