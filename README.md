# Test Automation

This project runs browser-based test cases from an Excel sheet and writes back Actual output and Status.

## Prerequisites

- Python 3.10+ (3.13 is OK)
- Internet access to the target site

## Setup

1. Create and activate a virtual environment (optional but recommended).
2. Install dependencies:

```
python -m pip install openpyxl playwright
python -m playwright install
```

## Run

From the project folder:

```
python test_automation.py --excel "Assignment- Test cases.xlsx"
```

## Common Options

- --excel: Path to the Excel file.
- --sheet: Sheet name (default: " Test cases").
- --headless: Run without visible browser UI.
- --url: Override target URL.
- --wait-ms: Wait time after clicking translate.
- --retries: Retry count for reading output.
- --type-delay-ms: Typing delay for input.
- --timeout-ms: Playwright timeout.
- --keep-open: Keep browser open after run.

## Output

The script updates the Excel file in place with:

- Actual output
- Status (PASS/FAIL/COLLECTED)

## Notes

- If the sheet uses different column names, the script tries to auto-detect them.
- If you want to save to a different file, use --output.
