# Applied AI for Earth Sciences (GEOL/ATMS 522)

Course materials for GEOL 522 / ATMS 522, *Applied AI for Earth Sciences*, a fully online graduate course at the University of Illinois Urbana-Champaign, first offered in Spring 2027. Instructor: Cristian Proistosescu.

This repository holds everything students see: the weekly concept notebooks, lab applications, homework (student versions), landing pages and the setup guide, built into a website with [Jupyter Book 2](https://jupyterbook.org). Solutions, quiz banks and lecture outlines are kept in a separate private repository; instructors who want to use these materials in their own course can request the solutions from the author.

## Running the notebooks

Start with the setup page, `week01_ml_workflow/W01_core0_setup.md`: it covers Google Colab (nothing to install) and a local installation from `environment.yml` (conda environment `geol522`), in VS Code or JupyterLab. Every notebook downloads the data it needs into a `data/` folder beside itself the first time it runs; no data are stored in this repository.

## Building the website

```
pip install jupyter-book     # Jupyter Book 2 (needs Node.js; it offers to install one)
jupyter book start           # live preview
jupyter book build --html    # static site in _build/html
```

## License

Text, figures and other non-code content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code, including the code cells of the notebooks: [MIT](LICENSE). See `LICENSE.md` for both. The CAMELS data used in the early weeks are by Addor et al. (2017), CC BY 4.0, and are downloaded from Zenodo at run time.

The materials were developed with the help of AI coding assistants and reviewed by the instructor; the course asks students to declare their own use of such tools, and this repository declares its own.
