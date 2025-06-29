# PyDBox - Python Data Science Toolbox

[![PyPI version](https://badge.fury.io/py/pydbox.svg)](https://badge.fury.io/py/pydbox)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/)

PyDBox is a comprehensive Python toolbox for data science and machine learning tasks. It provides a collection of tools and utilities to make data analysis and processing easier and more efficient.

## 📚 Publication

The TESI (Time-series Euclidean Space Interpolation) algorithm has been published in:

**Trigonometric-Euclidean-Smoother Interpolator (TESI) for continuous time-series and non-timeseries data augmentation for deep neural network applications in agriculture**  
*Computers and Electronics in Agriculture, Volume 206, 107646*  
Impact Factor: 6.757 (Q1)  
DOI: [10.1016/j.compag.2023.107646](https://doi.org/10.1016/j.compag.2023.107646)

If you use TESI in your research, please cite:
```bibtex
@article{TESI2023,
    title = {Trigonometric-Euclidean-Smoother Interpolator (TESI) for continuous time-series and non-timeseries data augmentation for deep neural network applications in agriculture},
    journal = {Computers and Electronics in Agriculture},
    volume = {206},
    pages = {107646},
    year = {2023},
    doi = {10.1016/j.compag.2023.107646}
}
```

## 🚀 Features

- **Modular Design**: Easy to use, extend, and integrate with existing workflows
- **Production Ready**: Thoroughly tested with comprehensive error handling
- **Performance Optimized**: Efficient implementations for handling large datasets
- **Pandas Compatible**: Seamless integration with pandas DataFrames
- **Type Hints**: Full type annotation support for better IDE integration

## 📦 Installation

```bash
pip install pydbox
```

## 🧰 Modules

### TESI (Time-series Euclidean Space Interpolation)

TESI is a powerful interpolation module that implements various methods for time series data using Euclidean space transformations. It's particularly useful for:
- Financial time series analysis
- Sensor data processing
- Scientific data interpolation
- Agricultural data analysis
- Deep learning data augmentation
- Any sequential data that requires sophisticated interpolation

#### Quick Start

```python
import pandas as pd
from pydbox.tesi import TESI

# Create sample data
df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6]
})

# Create TESI interpolator
interpolator = TESI(
    input_data=df,
    equation='Euc_p1',  # Linear interpolation
    augmentation_factor=5  # Generate 5 points between each pair
)

# Get interpolated data
result = interpolator.pd_frame()
print(result)
```

#### Available Interpolation Methods

| Method | Description | Best For |
|--------|-------------|----------|
| `Euc_p1` | Linear interpolation | Simple, monotonic data |
| `Euc_p2` | Quadratic interpolation | Smooth curves with moderate complexity |
| `Euc_p3` | Cubic interpolation | Complex curves with multiple inflection points |
| `Euc_Log` | Logarithmic interpolation | Data with exponential trends |

#### Advanced Features

- **Robust Value Handling**:
  - Zero values preservation
  - Near-zero value stability
  - NaN and infinity handling
  - Automatic data type conversion

- **Performance Optimizations**:
  - Vectorized operations
  - Memory-efficient processing
  - Parallel processing support for large datasets

- **Quality Assurance**:
  - Input validation
  - Numerical stability checks
  - Result verification

## 🔧 Configuration

TESI can be configured with various parameters:

```python
interpolator = TESI(
    input_data=df,
    equation='Euc_p1',
    augmentation_factor=5,
    zero_threshold=1e-10,  # Define what constitutes a "zero" value
    precision=1e-6,        # Numerical precision for calculations
    validate_input=True    # Enable/disable input validation
)
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please make sure to update tests as appropriate and adhere to our coding standards.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

- **Derraz Radhwane**
  - GitHub: [@derrazradhwanedz](https://github.com/derrazradhwanedz)
  - Email: derrazradhwanedz@gmail.com

## 📚 Documentation

For detailed documentation and examples, visit our [GitHub repository](https://github.com/derrazradhwanedz/pydbox).

## ✨ Coming Soon

- Additional interpolation methods
- GPU acceleration support
- Interactive visualization tools
- Real-time data processing
- More data science utilities

## 🙏 Acknowledgments

Special thanks to all contributors and users who have helped improve this package.