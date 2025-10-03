# Contributor Guidelines

Welcome to the ADS-505 Pharma Sales Forecast project! To keep the repository healthy and approachable for new collaborators, please follow the practices outlined below.

## Code style and linting
- Write Python code (scripts and notebook cells) that conforms to **PEP 8** conventions.
- Prefer vectorized pandas/numpy operations and descriptive variable names.
- When editing notebooks, keep cells focused and re-run the notebook top-to-bottom to ensure a clean, linear execution order.
- Run `ruff check .` (or at minimum `flake8`) on any Python modules or notebooks exported as scripts via `jupyter nbconvert --to script`.

## Testing and validation
- Before committing, restart the notebook kernel and execute all cells to confirm outputs are deterministic and free from hidden state.
- For scripts, add or update unit tests when logic changes and run `pytest` to ensure regression coverage.
- Validate data visualizations and metrics for consistency with prior runs; note any intentional changes in accompanying Markdown cells or commit messages.

## Notebook structure
- Alternate code and Markdown cells so that each analytical step is accompanied by a narrative explanation accessible to non-technical readers.
- Use Markdown headings that mirror the project outline (data loading, preprocessing, modeling, evaluation, conclusions).
- Keep configuration (imports, paths, constants) in the first code cell, followed by clearly labeled sections; place lengthy helper functions in separate `.py` modules when practical.

## Data management
- Store raw and intermediate datasets inside the `'Pharma Sales Data/'` directory.
- Do **not** commit large files (>50 MB) or sensitive data; add them to `.gitignore` and document download or generation steps in `README.md` or the relevant notebook.
- Use lightweight sample datasets for demonstrations and unit tests so repository clones remain manageable.

Thank you for helping maintain a clear and reproducible workflow!
