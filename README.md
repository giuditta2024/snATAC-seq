# snATAC-seq
Repository to try and test snATAC-seq analysis.


Initialize and match git repository:


```{code}
git init
git remote add origin https://github.com/giuditta2024/snATAC-seq.git
git branch -m master main   # rename master to main 
```
Remember to add the folder data/ to the .gitignore file. 


Then, download the required data:

```{code}
sh download_data.sh

# move them in the data folder
mv atac*.* data/
```

## Analysis in R

Refer to the Rmd.

> **Warning:** 
> *To be updated*


## Analysis in Python 

I will follow a couple of tutorials: 
- [Single Cell best practices](https://www.sc-best-practices.org/chromatin_accessibility/introduction.html)
- [EpiScanpy documentation](https://episcanpy.readthedocs.io/en/latest/examples.html)



Regarding python conda enviroment: 

```{code}
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge

conda create --name scATAC-env anndata matplotlib numpy pandas scanpy scipy scikit-learn seaborn
conda activate scATAC-env
conda install -c bioconda pyliftover bamnostic pysam

```

Now we want to add the conda enviroment to the jupyter notebook:

```{code}
conda install ipykernel
python -m ipykernel install --user --name=scATAC-env --display-name "Python (scATAC-env)"
```
