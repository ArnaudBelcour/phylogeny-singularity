# Singularity recipe for phylogeny

This singularity recipe contains:

- IQ-TREE version 2.0-rc1 (November 21, 2019)
- RAxML-NG v0.9.0
- MrBayes 3.2.7
- BEAST v1.10.4
- BEAGLE library v3.2.0 (PRE-RELEASE)

Using the Singularity recipe, you can create a Singularity container:

````
sudo singularity build phylogeny.sif Singularity
````

These tools can be called using:

````
singularity exec phylogeny.sif tool_exec
````

The **tool_exec** to use:

- **iqtree**
- **raxml-ng**
- **mb** for MrBayes
- **beast**