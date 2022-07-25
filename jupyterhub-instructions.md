# JupyterHub instructions for NCBI Codeathons
NCBI provides a JupyterHub for codeathon teams during the synchronous portions of our events.

## Logging in:
In a web browser, go to https://jupyterhub01.ncbi.nlm.nih.gov/.
You will be asked for a username and password.

Your username is the username portion of the email address you registered for the codeathon with, in all lowercase. So if your email is `User.Name@domain.com`, your JupyterHub username is `user.name`.

The first time you log in to the hub, you may select your own password. Whatever you enter will become your JupyterHub password for future logins.

## Storing data
Each participant has a home directory on the hub at `/home/jupyter-<username>`.
For sharing data between team members, we have also set up a data directory for each
team at `/home/<codeathon-name>-team-<team-number>`.
For large datasets, it may be better to use an AWS S3 storage bucket.
See the codeathon team for help setting this up.

## Installing Python packages for use in Jupyter
The hub has a limited number of commonly used Python packages installed for all users,
including `numpy`, `scipy`, `pandas`, and `BioPython`.
You will likely want to install your own packages.
To make them available within your Jupyter notebooks, you will need to create a conda environment and set up an IPython kernel to use the environment.

For help with conda environments see [Managing environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) from the Conda documentation.

First, log into the JupyterHub and open a terminal. From the "New" dropdown menu select "Terminal".
If this is your first time using conda on the hub, you'll have to initialize it and restart your shell:
```bash
conda init
source .bashrc
```

Next, create a new environment and install the IPython kernel package in it.
```bash
conda create --name my-env ipykernel
```

Finally, activate your environment and install the IPython kernel spec.
```bash
conda activate my-env
python -m ipykernel install --user --name my-env  --display-name "Python (my-env)"
```

On the hub homepage, you can now select "Python (my-env)" from the "New" dropdown menu
to create a notebook using your environment. You may need to refresh the page for it to appear.

You can install packages in your envirnonment using the `conda install` command in the terminal. Make sure that your environment is active when you run the command.

## Using R in Jupyter
You can also use R as your Jupyter notebook kernel.
It is best to use conda to manage your R packages.
To set up an R kernel, create a conda environment and activate it:
```bash
conda create --name r-env r-irkernel
conda activate r-env
```

Next, install the kernel specification:
```bash
R -e 'IRkernel::installspec(name = "my-r-env", displayname = "R (my-r-env)")'
```

On the hub homepage, you can now select "R (my-r-env)" from the "New" dropdown menu.
You can install packages in your envirnonment using the `conda install` command in the terminal. Make sure that your environment is active when you run the command.
