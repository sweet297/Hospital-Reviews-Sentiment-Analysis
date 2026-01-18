# Hospital Reviews Sentiment Analysis

A small project analyzing sentiment in hospital reviews, with notebooks for exploration/modeling and a script to generate a polished PDF report.

## Structure
- [code.ipynb](code.ipynb): Core notebook for data exploration and sentiment modeling.
- [hospital_sentiment.ipynb](hospital_sentiment.ipynb): Additional/alternate workflow for sentiment analysis.
- [hospital.csv](hospital.csv): Dataset of hospital reviews.
- [models/](models/): Saved model artifacts or outputs (if any).

## Quickstart (Windows)
1) Create and activate a virtual environment:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2) Install core utilities used by the scripts/notebooks:

```powershell
pip install jupyter reportlab html2image python-docx
```

Note: The notebooks may require additional packages (e.g., pandas, scikit-learn, nltk). Install them as needed when running cells.

## Working with the Notebooks
- Open [code.ipynb](code.ipynb) or [hospital_sentiment.ipynb](hospital_sentiment.ipynb) in VS Code.
- Select your Python interpreter (the virtual environment above) and run cells top-to-bottom.
- Adjust preprocessing/model configuration as desired and re-run.

## Data
- The dataset is in [hospital.csv](hospital.csv). Inspect columns within the notebooks to understand available features and labels, and adapt preprocessing accordingly.

## Generate the PDF Report
- The script reads [Final_Report.md](Final_Report.md) and writes a formatted PDF as `Final_Report.pdf`.
- Run from the workspace root:

```powershell
python markdown_to_pdf.py
```

- Dependencies: `reportlab` and `html2image`. The script first tries an HTML-based conversion (with MathJax for LaTeX) and falls back to ReportLab. For full LaTeX rendering via TeX, consider installing MiKTeX: https://miktex.org/download

## Inspect a Word Template (Optional)
- If you have a Word file named `Template for Reference.docx` in the workspace, you can print its structure:

```powershell
python read_template.py
```

- Dependency: `python-docx`.

## Tips
- Keep your environment consistent to reproduce results.
- Save trained models or outputs under [models/](models/) with clear filenames.
- Commit generated PDFs only if needed; they can be reproduced from the markdown.

## Next Steps
- If you want, I can scan the notebooks to produce a `requirements.txt` and a brief model evaluation summary section for the README. Let me know and I’ll add them.
