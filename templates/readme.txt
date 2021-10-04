This is copied directly from: https://github.com/ML-course/master/tree/master/templates
CREDITS: @joaquinvanschoren

Copy files to nbconvert template directory:
- HTML: .../anaconda3/lib/python3.6/site-packages/nbconvert/templates/html
- Latex: .../anaconda3/lib/python3.6/site-packages/nbconvert/templates/latex

Create Slides:
jupyter nbconvert --to slides --template jads.tpl filename.ipynb --SlidesExporter.reveal_theme=night --post serve

Export PDF: add '?print-pdf' to url and remove '#'

Create Latex PDF:
jupyter nbconvert --to pdf --template jads.tplx filename.ipynb


JupyterLab setup:

* Jupyter Widgets

    jupyter labextension install @jupyter-widgets/jupyterlab-manager

EXTRA:

* Added dependency on entr for file watching

  ```sudo apt install entr```

  To run slides for a nb:
  ```ls *.ipynb | entr -r jupyter nbconvert --output-dir slides_html --to slides --template jads.tpl 00_Lecture_MLOPS.ipynb --SlidesExporter.reveal_theme=serif --ServePostProcessor.open_in_browser=False --post serve```

