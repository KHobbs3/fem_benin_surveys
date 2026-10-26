# FEM-Benin-Formative-Research-2026

Streamlit dashboard for the Benin FEM formative research survey (2026). It reads only
pre-aggregated CSVs, never respondent-level data. `../pipeline_output/pipeline/run_pipeline.py`
writes them to `data/`. The app loads its copies from Google Drive by file ID
(`src/data_loader.py`), so after re-running the pipeline, upload the changed CSVs to Drive and
update the IDs if the files are new.

```bash
pip install -r requirements.txt
streamlit run app.py
```

- `app.py` — Benin flag banner, title, English toggle, and the three sections: Baseline vs.
  Follow-up, Formative Research, and Phone Pulse.
- `src/page_*.py` — one module per tab. Phone Pulse hasn't been fielded in Benin, so its tabs
  are stubs (`page_stubs.py`).
- `src/data_loader.py` — loads the CSVs; `src/translations.py` — the AI-translated English toggle;
  `src/fem_colours.py` — palette.
