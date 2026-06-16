# Pandas Project Context

Welcome to the **Pandas** repository. This project focuses on leveraging the powerful data manipulation and analysis capabilities of the pandas library to solve [insert specific use case, e.g., data cleaning pipelines / financial data analysis / automated reporting].

## Project Goal
To provide clean, efficient, and reproducible data workflows using the pandas ecosystem.

## Key Principles for AI Assistants
When working with this codebase, please adhere to these principles:

1.  **Pandas Best Practices:** Avoid using iterative loops (like `for` rows in df) where vectorization is possible. Always prefer native pandas methods (`apply`, `map`, `groupby`, `merge`, etc.) for performance.
2.  **Memory Management:** Be mindful of memory usage when processing large datasets. Use appropriate data types (e.g., `category` for low-cardinality strings, `int32` instead of `int64` if possible).
3.  **Data Integrity:** Always validate inputs and outputs of transformation functions. Ensure that indexes are handled correctly to prevent alignment errors.
4.  **Reproducibility:** When writing transformation logic, ensure the code is deterministic and easy to audit.
5.  **Documentation:** Clearly document the expected schema (column names, types) of input and output DataFrames.

## Key Directories
* `data/`: Raw and processed data files (should be excluded from git, but relevant for path references).
* `notebooks/`: Exploratory data analysis (EDA) and prototype scripts.
* `src/`: Production-ready transformation scripts and helper functions.
* `tests/`: Test suites using `pytest` to validate data transformations.

## Coding Standards
* **Vectorization:** Prioritize NumPy/Pandas vectorized operations for speed.
* **Method Chaining:** Where appropriate, use method chaining to improve readability of transformation pipelines.
* **Type Hinting:** Use `pd.DataFrame` or `pd.Series` in type hints to make the code more self-documenting.

## Workflow
* **Analysis:** If the user presents a data problem, first analyze the structure (columns, types, missing values) before suggesting a solution.
* **Debugging:** When debugging, always suggest checking `df.head()`, `df.info()`, and `df.isnull().sum()` to narrow down issues.
* **Safety:** Never suggest destructive operations (e.g., `inplace=True` or `drop`) without ensuring the user has a backup or a way to verify the result.

---
*Last updated: 2026-06-16*
