STELLAR Space Weather Workshop tutorials
========================================

This is a repository to hold the notebooks that will be used throughout the STELLAR Space Weather Workshop [workshop](https://lofar.ie/stellar-sww/) 

Each hands-on session is in its own directory - i.e. the day one hands on session is in `day1_solar_sources` etc. 

## Run in Binder
If you don't want to run these locally, or you are having issues with getting them started - all the notebooks in this repository can be run with binder. Click here [![Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/TCDSolar/STELLAR_SSW_tutorials/HEAD) to launch binder and then run the notebooks in your browser: 
. 

It may take a few minutes to load up the first time you launch it.

## Run locally

Here are the steps you'll need to run:

#### 1. Download the files using git

If you want to run these notebooks locally you can clone this reposity (or fork it and then clone it from your page). To do this run this command:

- ```git clone  https://github.com/TCDSolar/STELLAR_SSW_tutorials```

If you have first forked it then you can run:

- ```git clone  https://github.com/<username>/STELLAR_SSW_tutorials```




#### 2. Create a conda environment

We recommend creating a new conda environment and install the requried packages used in these notebooks. [Here](https://towardsdatascience.com/getting-started-with-python-environments-using-conda-32e9f2779307) is a nice introduction to anaconda environments for those new to the concept. [Here](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) is a conda cheatsheet which may help too! 

The python packages required to run these workshop notebooks are listed in the `environment.yaml` file in this repository. To create a new environment with these packages installed you can open a terminal and type:

- ```conda env create -f environment.yml```

This will then create a new conda environment called `stellar_ssw` (this name is listed in the `enviroment.yaml` file).

You can then activate this environment by typing:

- ``` conda activate stellar_ssw```

Note your prompt should change and now have ‘stellar_sww’ near the start. If you want to list all your conda environments you can type
``` conda info -e```. You should see `base` which is your base enviroment, the `stellar_ssw` one, and any others you have created! 

##### 2.2 Updating the environment.yaml file
If an update is made to the `enviroment.yaml` file then you will need to type 

- ```conda env update --file environment.yml --prune```


### 3. Start a jupyter notebook!

Once you have your environment activated (remember to first type `conda activate stellar_ssw`) then in your local STELLAR_SSW repository type

- ```jupyter notebook ```

This should then open the notebooks in your default browser!

If you are having any issues - just make sure first that you are in the `stellar_ssw` environment before you start jupyter.

Happy coding!!


#### 4. Pulling the most up-to-date version
Throughout the workshop, these notebooks were updated and further notebooks were added. To make sure that your local repository reflects whats currently here you will need to run a `git pull`. This will pull the most up-to-date version of this repository. Before you do this however, you will want to check which remote you have linked to this repository. To find out this you can type this in your local STELLAR_SSW repository:

- ```git remote -v``` 

and this will list the current remotes
It might looks something like this

```
origin	https://github.com/<username>/STELLAR_SSW_tutorials.git (fetch)
origin	https://github.com/<username>/STELLAR_SSW_tutorials.git (push)
upstream	https://github.com/TCDSolar/STELLAR_SSW_tutorials (fetch)
upstream	https://github.com/TCDSolar/STELLAR_SSW_tutorials (push)
```

what you will want to do is pull the main branch from the one that is linked to `https://github.com/TCDSolar/STELLAR_SSW_tutorials` - which in this example is `upstream`. Hence to pull the latest version of this repository you would type:

- `git pull upstream main` 

and this will update your local files. 

Otherwise if when you typed `git remote -v` and it looks like
```
origin	https://github.com/TCDSolar/STELLAR_SSW_tutorials  (fetch)
origin	https://github.com/TCDSolar/STELLAR_SSW_tutorials  (push)
```
then you would type

- ``` git pull origin main```

to update your local files. 



