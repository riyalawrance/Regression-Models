## Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

### Required Libraries

```bash
pip install numpy matplotlib pandas scikit-learn
```

Or install from requirements.txt:
```bash
pip install -r requirements.txt
```

### Setup

1. Clone the repository
```bash
git clone https://github.com/yourusername/polynomial-regression-analysis.git
cd polynomial-regression-analysis
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Prepare your data
- Place your dataset as `Data.csv` in the project directory
- Ensure the last column contains the target variable (Y)
- All other columns will be used as features (X)

4. Run the analysis
```bash
python linear_regression.py
python polynomial_regression_degree2.py
python polynomial_regression_degree3.py
```

## Usage

### Dataset Format
Your `Data.csv` should be structured with:
- Features in all columns except the last
- Target variable in the last column

Example:
```csv
feature1,feature2,target
1.2,2.3,5.1
2.1,3.4,7.2
3.0,4.1,9.8
```

### Running the Models

**Linear Regression:**
```python
python linear_regression.py
```

**Polynomial Regression (Degree 2):**
```python
python polynomial_regression_degree2.py
```

**Polynomial Regression (Degree 3):**
```python
python polynomial_regression_degree3.py
```

### Model Output
Each model provides:
- **R² Score**: Coefficient of determination (higher is better)
- **SSE**: Sum of Squared Errors (lower is better)
- **Visualizations**: Scatter plots with regression lines for training and test sets

### Example Output
```
Coefficient of Determination R^2 = 0.8542
SSE = 142.35
```

## Project Structure

```
polynomial-regression-analysis/
├── linear_regression.py              # Linear regression implementation
├── polynomial_regression_degree2.py  # Quadratic regression implementation
├── polynomial_regression_degree3.py  # Cubic regression implementation
├── Data.csv                          # Dataset file
├── requirements.txt                  # Python dependencies
├── README.md                         # Project documentation
└── plots/                           # Generated visualization plots
    ├── linear_train.png
    ├── linear_test.png
    ├── poly2_train.png
    ├── poly2_test.png
    ├── poly3_train.png
    └── poly3_test.png
```

## Model Comparison

| Model | Complexity | Use Case |
|-------|------------|----------|
| Linear | Low | Simple relationships, baseline model |
| Degree 2 | Medium | Quadratic relationships, curved patterns |
| Degree 3 | High | Complex curves, non-linear patterns |

### Performance Metrics

The project evaluates models using:
- **R² Score**: Measures how well the model explains variance
- **SSE**: Sum of squared errors between actual and predicted values

## Configuration

### Data Split Configuration
- **Test Size**: 40% (0.4)
- **Random State**: 2 (for reproducible results)
- **Train Size**: 60% (remaining data)

### Customization Options
You can modify these parameters in each script:

```python
# Change test size (default: 0.4)
X_Train, X_Test, Y_Train, Y_Test = train_test_split(X, Y, test_size=0.3, random_state=2)

# Change random state for different data splits
X_Train, X_Test, Y_Train, Y_Test = train_test_split(X, Y, test_size=0.4, random_state=42)

# Modify polynomial degree (for polynomial regression)
poly_features = PolynomialFeatures(degree=4)  # Try degree 4 or higher
```

## Development

### Running Individual Models
```bash
python linear_regression.py          # Run linear regression
python polynomial_regression_degree2.py  # Run quadratic regression
python polynomial_regression_degree3.py  # Run cubic regression
```

### Adding New Polynomial Degrees
To add higher degree polynomials:

1. Create a new file (e.g., `polynomial_regression_degree4.py`)
2. Modify the polynomial features:
```python
from sklearn.preprocessing import PolynomialFeatures
poly_features = PolynomialFeatures(degree=4)
```

### Visualizations
The project generates scatter plots showing:
- **Red dots**: Actual data points
- **Blue line**: Regression line/curve
- Separate plots for training and test sets

### Requirements File
Create `requirements.txt`:
```
numpy>=1.21.0
matplotlib>=3.4.0
pandas>=1.3.0
scikit-learn>=1.0.0
```

## Results & Analysis

### Expected Outputs

Each model will output:
1. **Coefficient of Determination (R²)**: Value between 0 and 1
2. **Sum of Squared Errors (SSE)**: Lower values indicate better fit
3. **Visualization plots**: Training and test set scatter plots with regression lines

### Model Selection Guidelines

- **Use Linear Regression** when data shows linear relationships
- **Use Degree 2 (Quadratic)** for data with curved patterns
- **Use Degree 3 (Cubic)** for more complex, non-linear relationships
- **Compare R² scores** to determine the best-fitting model

### Overfitting Warning
Higher degree polynomials may overfit to training data. Always compare performance on test sets.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/NewRegressionModel`)
3. Add your regression implementation
4. Test with sample data
5. Commit your changes (`git commit -m 'Add polynomial degree 4 regression'`)
6. Push to the branch (`git push origin feature/NewRegressionModel`)
7. Open a Pull Request

### Ideas for Contributions
- Add higher degree polynomial models
- Implement Ridge or Lasso regression
- Add cross-validation techniques
- Improve visualization with seaborn
- Add feature scaling/normalization
- Create batch processing for multiple datasets

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you have any questions or run into issues, please:
- Check the [Issues](https://github.com/yourusername/polynomial-regression-analysis/issues) page
- Create a new issue with:
  - Your dataset format
  - Error messages (if any)
  - Expected vs actual behavior
- Contact: your.email@example.com

### Common Issues
- **FileNotFoundError**: Ensure `Data.csv` is in the project directory
- **Import Errors**: Install all required packages using `pip install -r requirements.txt`
- **Empty Plots**: Check if your dataset has the correct format

## Acknowledgments

- **scikit-learn**: For machine learning algorithms and utilities
- **matplotlib**: For data visualization
- **pandas**: For data manipulation and analysis
- **numpy**: For numerical computations
- Machine learning community for regression techniques and best practices

---

**Made with ❤️ by [Your Name](https://github.com/yourusername)**
