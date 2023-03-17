# Template: Interactive Notebook in R 

This is a template for creating a Jupyter Notebook in R, created for NOAA RESTORE's:

**Oysters, Blue Crabs, and Spotted Seatrout:** ***Building Resilience to Environmental Trends and Variability in the Gulf of Mexico***

Using GitHub and Binder, share your work:
- Describe your project
- Add Lat/Lon information to make an interactive map of the study area and for station data
- Do plots and analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OyBcSt/project-template-r/HEAD?labpath=index.ipynb)

This example repo uses R.  ([Using Python? Check Here.](https://github.com/OyBcSt/project-template-python))

## How to use the template to make your own repo

Starting from the landing page of the repo, click the green button `Use this template` then choose `Create a new respository`.

Choose the Owner
- If your project is NOAA RESTORE, please change `Owner` to `OyBcSt`.  
- If you don't see OyBcSt as an option, Contact [Lisa](mailto:lllowe@ncsu.edu) to be added as a collaborator.  

Choose the Repository name
- Choose something that indicates the *type* of project, e.g., hydro, climate, fisheries, etc.

Modify the README
- Change the **README.md**.  Click the pencil, and edit it directly to describe your project.
- Change the address for the Binder button...remember, the button is pointing at the *template*.  See below.
- [For Reference: GitHub markdown syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

How to get the Binder button code:
- Go to https://mybinder.org (in a new tab).
- Paste the URL to *your new repo*.
- Put `index.ipynb` in the box for File.
- Where it says `Expand to see...`, click and copy the Binder button code.

Test the Binder button:
- Click the modified Binder button, and verify a working Notebook is being launched from *your new repo*.

## How to modify the repo

Much can be edited directly from GitHub (clicking pencils).  Edits to the Notebook while in Binder are not saved to GitHub.  When modifying the Notebook in Binder, periodically `Save Notebook`, then `Download` the file locally.  Then the local files must be added back to GitHub.

### No *git* for me please!
To add local files back to the repo, go to the GitHub page, click `Add file`, then `Upload files`.

### A bit of *git*
If you do lots of changes, `Upload files` will get old fast. 

Personally, I clone the repo locally, from Mac terminal:
```
git clone [https://address/reponame]
cd reponame
```

Then, I modify things while in Binder, `Save Notebook`, `Download`, and I download to `reponame`.  Then, from my Mac terminal, I do
```
git status
```
Check the status.  The index.ipynb is probably the only thing that changed.  And if it **should** have changed but **didn't**, you might want to `Save` and `Download` again.  Then:
```
- git add .
- git status
- git commit -m "added more notebook"
- git push
```

If you were modifying the **README.md** online, you will need to pull those in before pushing out your changes:
```
- git pull
```

**Contact me if you need help with git**.  We can develop some training and documentation based on what folks are having problems with.

### Do I have to use Binder to develop the Notebook?
Nope.  If you are actively working on something, you probably want to develop locally.

Beginners:
- Download Anaconda
- Open and develop the Notebook in Jupyter
- Use git (as above) to push changes
- See:[How to use the R programming language in Jupyter Notebook](https://docs.anaconda.com/navigator/tutorials/r-lang/)

Binder has to build your environment.  If new libraries are needed for script modifications, you may need to change the runtime, or install new packages.  That is what these files do:
- runtime.txt
- install.R

Not Beginners:
- It is better to install miniconda, create a yaml file with dependencies, then `conda env create`, for each project.  
- [See this for more about Conda](https://hpc.ncsu.edu/Software/Apps.php?app=Conda)
- Unfortunately, I did not test running a Notebook with **R** using miniconda...but we'll figure it out.

**Contact me if you need help with the environment.**. We can develop some extra documentation based on what folks are having problems with.


*This work is funded by the National Oceanic and Atmospheric Administration's RESTORE Science Program under award NA19NOS4510194.*

