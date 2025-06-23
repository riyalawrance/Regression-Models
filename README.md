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
git clone https://github.com/yourusername/polynomial-regression-analysis.git
cd polynomial-regression-analysis
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
2. Open `Polynomial_Regression_Analysis.ipynb`
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

- `Polynomial_Regression_Analysis.ipynb` - Main notebook
- `Data.csv` - Your dataset
- `requirements.txt` - Dependencies

## Contributing

1. Fork the repo
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details.
