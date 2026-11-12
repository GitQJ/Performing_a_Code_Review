# Performing_a_Code_Review
Reviewed a data analysis workflow for adherence to Python standards and best-practices

## Python Code Review: Refactoring Smartphone Data Prep for PEP-8, DRY and pytest Unit Tests | Python, pandas

Reviewed and refactored a smartphone data-preparation and plotting workflow to meet Python best practices: accurate documentation, PEP-8 style, no duplicated logic and a passing pytest unit test.

# CONTEXT
Data teams ship code to production, and code review catches logic and style issues missed during development. The scenario: review a colleague's function that cleans smartphone data from a CSV and plots features against price, ahead of a procurement decision.

# MY ROLE
I acted as the reviewer, editing both the code and the test.

# WHAT I DID
• Documentation and readability: aligned the docstrings with what the code actually does, fixed comments and removed a debug print
• PEP-8: Refactor spacing, naming, line length and imports according to conventions
• DRY: refactored visualize_versus_price() to reuse column_to_label() instead of repeated label-formatting logic
• Testing: reworked test_nan_values so it checks the same columns the cleaning function filters (battery_capacity and os), then ran it with ipytest until it passed with ExitCode.OK

# RESULTS
• Docstrings, comments and code now agree with each other
• Label logic lives in one function, so a label change is made in one place
• Unit test passes (ExitCode.OK)
• 25 of 980 rows removed by the cleaning steps

# TECH STACK
Python, pandas, seaborn, Matplotlib, pytest, ipytest
