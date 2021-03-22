# pandas-hacks
Repo showing some neat packages for Pandas

## Quickstart

1. [Install Anaconda](https://www.anaconda.com/products/individual)
2. [Install direnv](https://direnv.net/docs/installation.html) (Optional)
3. Clone this repo: `git clone https://github.com/Tommo565/pandas-hacks.git` and `cd` into the repo `cd pandas-hacks`
4. [Create a service account](https://cloud.google.com/iam/docs/creating-managing-service-accounts) with BigQuery > Editor permissions. This will allow Python and Jupyter to interact with Bigquery. 
5. [Create a service account key](https://cloud.google.com/iam/docs/creating-managing-service-account-keys) and save this somewhere outside of the repo.
6. If using direnv, create an `.envrc` file and a `GOOGLE_APPLICATION_CREDENTIALS` variable with the path to your credentials file. You should be prompted to execute `direnv allow` in the command line. This will load the variable into your environment automatically. The file should look like this:

```bash
export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service_account_key.json"
```

7. If not using direnv, you will need a create a GOOGLE_APPLICATION_CREDENTIALS variable in the notebook as follows:
```python
import os

os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "path/to/your/service_account_key.json"
```

7. Create the conda environment `conda env create -f env.yml`
8. Install the environment into Jupyter `python -m ipykernel install --name pandas-hacks`
9. Start the Jupyter notebook `jupyter notebook`

## Contents

The notebooks in the `notebooks` folder contain overviews for the following pandas packages:
* pandas-gbq
* pandas-profiling
* dtale

