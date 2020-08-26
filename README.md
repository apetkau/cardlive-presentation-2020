# CARD:Live Presentation code

This repo contains supplementary code (as a [Jupyter notebook][]) for a presentation on the [CARD:Live][] dashboard. This will walk you through using [Python Dash][] to create an interactive dashboard and plot geographic information.

# Code

The code (as a Jupyter Notebook) is available in the file [cardlive-presentation-code.ipynb][]. To run please install the below dependencies and then do:

```bash
conda activate cardlive-presentation
juptyer lab
```

You should now have Juptyer Lab running on <http://localhost:8888> where you can load up the Juptyer notebook.

# Dependencies

To run the Jupyter notebook locally you will need to install a number of dependencies. Please first install [conda][] and then run the following commands to install the rest of the dependencies:

```bash
# Create/activate conda environment
conda env create -f environment.yml
conda activate cardlive-presentation
```

The Dash/Plotly/Jupyter integration requires some additional commands given below:

```bash
# First install nodejs. I could not get the proper version installed via conda so I am installing from the website.
mkdir dependencies
cd dependencies
wget https://nodejs.org/dist/v12.18.3/node-v12.18.3-linux-x64.tar.xz
tar -xvvf node-v12.18.3-linux-x64.tar.xz
export PATH=$PWD/node-v12.18.3-linux-x64/bin:$PATH

# Step 2: Install Jupyter Plotly extension
jupyter labextension install jupyterlab-plotly
```

[CARD:Live]: https://card.mcmaster.ca/live
[Python Dash]: https://plotly.com/dash/
[cardlive-presentation-code.ipynb]: cardlive-presentation-code.ipynb
[Jupyter notebook]: https://jupyter.org/
[conda]: https://docs.conda.io/en/latest/miniconda.html
