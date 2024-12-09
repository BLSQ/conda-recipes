# Dependencies
In order to build the recipes, you need to install the following dependencies:
```bash
conda install conda-build anaconda-client
```

# How to release a new version of the recipes

1. Update the version number and associated sha in the `meta.yaml` file of each recipe.
2. Run `conda build <recipe>  --channel conda-forge --channel bioconda` to build the recipe.
3. Run `anaconda upload <path_to_built_package>` to upload the package to the `openhexa` channel on Anaconda Cloud.

It's possible that your anaconda config is set to automatically upload the packages. Check the output of the `anaconda upload` command to see if it's the case.