# Code & Env Setup

### Code Setup

In general, there are three workflows you can use to edit code and run it on the cluster:

1. Sign on through the Terminal and use an editor like emacs, vim, or nano to edit code directly in the terminal on the cluster.
2. Edit your code locally and then copy it up to the cluster using either [scp](https://www.geeksforgeeks.org/scp-command-in-linux-with-examples/), [rsync](https://www.geeksforgeeks.org/rsync-command-in-linux-with-examples/), or pushing to a remote repo that is cloned on the cluster.
3. Sign onto the cluster through an editor like VS code, and edit your files directly on the cluster compute.

Here, we walk through workflow #3. However, if you are running into latency problems interacting with the cluster through VS code directly, you may consider using workflow #2.

1. Clone your code repo.\
   <img src="../.gitbook/assets/Screenshot 2024-06-07 at 11.15.49 AM.png" alt="" data-size="original">\
   \
   ![](<../.gitbook/assets/Screenshot 2024-06-07 at 11.16.18 AM (1).png>)\

2. Type the name of your repo.\
   ![](<../.gitbook/assets/Screenshot 2024-06-07 at 11.16.38 AM.png>)

Your repo will then be setup on the cluster.

### Environment Setup

You can use any environment management strategy you prefer. Our example below shows how to set up a [conda](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html) environment.

1. Create a new environment.

```bash
# Standard environment creation:
$ conda create --name <environment-name>

# If you want to setup the environment in a particular location, use this instead:
$ conda create --prefix /path/to/environment/directory
```

1. Activate your environment.

```bash
# For the fist setup method above:
$ conda activate <environment-name>

# For the second setup method above:
$ conda activate /path/to/environment/directory
```

1. Setup [pip](https://pypi.org/project/pip/).

```bash
# This will make sure packages are installed in your environment
(environment-name)$ conda install pip
```

1. Install any packages you need to run your code. For example, if you have a requirements file:

```bash
(environment-name)$ pip install -r requirements.txt
```

Now you are ready to run your jobs. Before submitting a job to the cluster, make sure your environment is activated. Alternately, you can activate your environment in your job script.
