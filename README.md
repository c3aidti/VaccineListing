# Vaccine Listing Example

The C3 Covid-19 Datalake contains data about ongoing clinical trails related to covid 19. This notebook explores how to fetch this data, transform it into a usable form, and some simple data analysis.

## Python Implementation

The python implementation of this example is located in the `python` directory. This example can be run with any python environment containing a jupyter notebook installation and requests and pandas libraries.

We provide a conda environment definition file `env.yaml` which should work as well. To provision an appropriate conda environment run `conda env create -f env.yaml -p <path_to_prefix>` or `conda env -f env.yaml -n <name_of_environment`.

Once an appropriate environment is set up, launch the jupyter notebook, and execute the cells within.

## C3 Implementation

The C3 implementation of this example is in the directory `c3-python-connector`. Make sure you have access to a C3 tag which has the Datalake package provisioned either directly, or as a dependency of your current package. To ensure your python environment has everything needed, we recommend provisioning a conda environment with

```
conda env create -f ./env.yaml -p ./venv
```

After which you can launch jupyter notebook, and open the notebook `casesExample.ipynb`.

When running the jupyter notebook, there's a cell at the top meant to connect to a running C3 tag. If you're running python/jupyter 'remotely' that is not through C3's system, you will need to replace the `<vanity_url>`, `<tenant>`, and `<tag>` in the cell negotiating the connection to C3. It should look like this:

```
c3 = get_c3('<vanity_url>', '<tenant>', '<tag>')
```
