# PyDBox - Python Data Science Toolbox

PyDBox is a comprehensive Python toolbox for data science and machine learning tasks. It provides a collection of tools and utilities to make data analysis and processing easier.

## Installation

```bash
pip install pydbox
```

## Modules

### TESI (Time-series Euclidean Space Interpolation)

TESI is a powerful interpolation module that implements various methods for time series data using Euclidean space transformations.

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

#### TESI Features

- Multiple interpolation equations:
  - Linear (`Euc_p1`)
  - Quadratic (`Euc_p2`)
  - Cubic (`Euc_p3`)
  - Logarithmic (`Euc_Log`)
- Robust handling of:
  - Zero values
  - Near-zero values
  - Sparse data
  - Various data distributions
- Easy-to-use pandas DataFrame interface
- Numerical stability with small values
- Configurable precision and zero-value threshold

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

- **Derraz Radhwane** - [GitHub](https://github.com/derrazradhwane)
- Email: derrazradhwanedz@gmail.com 