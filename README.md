[![Binder](https://mybinder.org/badge_logo.svg)][binder-link]

# CARD:Live Presentation code

This repo contains supplementary code (as a [Jupyter notebook][]) for a presentation on the [CARD:Live][] dashboard. This will walk you through using [Python Dash][] to create an interactive dashboard and plot geographic information.

# Getting started

The easiest way to run this code is via [binder][]. This will launch a virtual machine in the cloud with all the dependencies installed and open up Juptyer for you to follow along.

To get started, please click the following: [![Binder](https://mybinder.org/badge_logo.svg)][binder-link]

*Note: The Dash portion of the Juptyer notebook does not work in Binder. However, all the other code (Python pandas, geopandas, and plotly) will work.*

# Local installation

Instead of Binder, if you wish to install and run this code locally please install the below dependencies and run the following.

```bash
conda activate cardlive-presentation
juptyer lab
```

You should now have Juptyer Lab running on <http://localhost:8888> where you can load up the Juptyer notebook. You can also view the Jupyter Notebook at [cardlive-presentation-code.ipynb][].

## Dependencies

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
[binder-link]: https://mybinder.org/v2/gh/apetkau/cardlive-presentation-2020/presentation-v1?filepath=cardlive-presentation-code.ipynb
[binder]: https://mybinder.org/
