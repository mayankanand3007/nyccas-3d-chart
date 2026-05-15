# NYCCAS 3D Control Chart

Short description
-----------------

An interactive 3D control-chart visualization of seasonal borough measurements from the NYCCAS-derived CSV. Built with Three.js and intended for exploratory and presentation use in academic settings.

Abstract
--------

This project visualizes seasonal borough-level measurements (see `data_csv/NYCCAS-Seasonal-Borough.csv`) in a 3D control-chart layout. The visualization computes mean, standard deviation, and control limits (UCL/LCL) from the data and highlights out-of-control points. It is designed to accompany academic talks, posters, or reproducible demonstrations.

Files
-----

- `borough_seasonal_control_chart.html` — main interactive visualization (open in a browser)
- `data_csv/NYCCAS-Seasonal-Borough.csv` — source data (CSV)
- `CITATION.cff` — citation metadata for this project
- `LICENSE` — license (MIT)

How to view locally
-------------------

The visualization is self-contained and can be opened directly in a browser, but some browsers restrict file-based fetches. Serve the folder with a simple HTTP server and open the page:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/borough_seasonal_control_chart.html
```

Requirements
------------

- A modern web browser (Chrome, Firefox, Safari) with WebGL enabled. The page loads Three.js from a CDN.

Reproducibility and screenshots
-----------------------------

1. Start a local server (see above).
2. Open the page and interact with the view to the desired framing.
3. Take screenshots using the browser or a headless browser. For example, with Chromium installed:

```bash
# start server in repo root
python3 -m http.server 8000
# in another terminal (mac/linux)
google-chrome --headless --screenshot=chart.png --window-size=1200,800 http://localhost:8000/borough_seasonal_control_chart.html
```

Citation
--------

Please cite this project if you use it in academic work. See `CITATION.cff` for machine-readable metadata and the BibTeX entry below:

```bibtex
@misc{nyccas-3d-control-chart,
  title = {NYCCAS 3D Control Chart},
  author = {Add Author Name},
  year = {2026},
  note = {Interactive visualization; data: NYCCAS Seasonal Borough CSV},
  url = {https://your-repo-url}
}
```

License
-------

This repository is released under the MIT License — see `LICENSE`.

Contact
-------

If you want help preparing slides, creating static figures, or adding a DOI, open an issue or update `CITATION.cff` with the proper metadata.