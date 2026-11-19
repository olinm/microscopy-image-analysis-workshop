# From pixels to protein degradation

This is the browser edition of a beginner-friendly microscopy image-analysis
workshop based on a real tAKT degrader experiment.

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olinm/microscopy-image-analysis-workshop/blob/main/01_WORKSHOP_COLAB.ipynb)

## Start the workshop

1. Click **Open in Google Colab** above.
2. Sign in to Google if asked.
3. Choose **Runtime → Change runtime type** and select runtime version
   **2026.07 (Python 3.12)**. Leave the hardware accelerator as **None**.
4. Run the first package-installation cell. It restarts Colab once; this is
   expected.
5. Reconnect, rerun that cell once, and then continue cell by cell.

No local Python, Conda, VS Code or Git installation is required.

## What the notebook covers

- viewing Hoechst, HCSGreen and tAKT-A647 microscopy channels;
- measuring fluorescence from supplied whole-cell masks;
- testing Cellpose whole-cell segmentation on a crop;
- testing StarDist nuclear segmentation on a crop;
- matching cells and nuclei;
- interactive browser-based mask and channel inspection;
- quality control and area filtering;
- Hoechst-based cell-cycle gating;
- treatment comparison using the real processed experiment.

The Colab notebook uses a small real image field and 216 real per-field CSV
tables. `colab_workshop_data.zip` is downloaded automatically by the notebook.

## Local version

The browser notebook is intended for the workshop itself. The separately tested
local version remains preferable for adapting the pipeline to new datasets and
for interactive mask editing in napari.

## Important Colab note

Google Colab runtimes are temporary. Files and installed packages disappear
after the runtime is deleted, but the original notebook and workshop data in
this repository are unaffected.

The workshop currently requires Python 3.12 because StarDist does not yet
support Colab's Python 3.13 runtime. Colab does not remember the selected past
runtime between sessions, so check **Runtime version: 2026.07** each time you
start a new workshop session.
