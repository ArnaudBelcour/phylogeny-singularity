# Singularity recipe for phylogeny

This singularity recipe contains:

- BEAGLE library v3.2.0 (PRE-RELEASE)
- BEAST v1.10.4
- FastME 2.1.6.1
- FastTree 2.1
- IQ-TREE version 2.0-rc1 (November 21, 2019)
- MrBayes 3.2.7
- PhyML v3.3.20190909
- RAxML-NG v0.9.0

Using the Singularity recipe, you can create a Singularity container:

````
sudo singularity build phylogeny.sif Singularity
````

These tools can be called using:

````
singularity exec phylogeny.sif tool_exec
````

The **tool_exec** to use:

- **beast**
- **fastme**
- **FastTree**, **FastTreeDbl** and **FastTreeMP** for FastTree
- **iqtree**
- **mb** for MrBayes
- **phyml** and **phyml-mpi** for PhyML
- **raxml-ng**