# lokstats

**lokstats** is a Python package for advanced statistical calculations, specializing in multiple and partial correlations. It provides two simple functions to compute:

1. **Multiple Correlation** (`mulcor`)
2. **Partial Correlation** (`partcor`)

---

## Table of Contents

* [Installation](#installation)
* [Features](#features)
* [Usage](#usage)

  * [mulcor](#mulcor)
  * [partcor](#partcor)
* [Development](#development)
* [License](#license)

---

## Installation

Install directly from PyPI (when published):

```bash
pip install lokstats
```

Or clone the repo and install locally:

```bash
git clone https://github.com/loksundar/partial_multiple_correlation.git
cd partial_multiple_correlation
pip install .
```

---

## Features

* **mulcor**: Calculate the multiple correlation coefficient for a target variable against all other predictors in a DataFrame.
* **partcor**: Calculate the partial correlation coefficient between two variables, controlling for the influence of others.

---

## Usage

Import the package and call the functions on your Pandas DataFrame:

```python
import pandas as pd
from lokstats import mulcor, partcor

# Load your data
df = pd.read_csv('your_data.csv')

# 1. Compute Multiple Correlation
#    - dataframe: df
#    - column: name of the target variable
mult_corr = mulcor(df, 'target_column')
print(f"Multiple Correlation for 'target_column': {mult_corr}")

# 2. Compute Partial Correlation
#    - dataframe: df
#    - var1: name of the first variable
#    - var2: name of the second variable
partial_corr = partcor(df, 'column1', 'column2')
print(f"Partial Correlation between 'column1' and 'column2': {partial_corr}")
```

For more detailed examples and data inputs, see the full repository at: [https://github.com/loksundar/partial\_multiple\_correlation](https://github.com/loksundar/partial_multiple_correlation)

---

## Development

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
