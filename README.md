# Pairing Metagenomics and Metaproteomics to Pinpoint Ecological Niches and Metabolic Essentiality of Microbial Communities 
This repository contains scipts needed to compare the gene-level functional redundancy $\text{FR}_g$ and the protein-level functional redundancy $\text{FR}_p$. The comparison between $\text{FR}_g$ and $\text{FR}_p$ enables us to understand the ecological and metabolic roles of each protein function. A preprint that describes the method in detail can be found [here](). 
![schematic](schematic.png)

## Versions
The version of Python we used is 3.7.3.

## Dependencies
Necessary Python packages can be found in `requirements.txt`. Installing those packages can be achieved by pip:
```
pip install -r requirements.txt
```

The entire installation process takes less than half an hour for the setting we used (Macbook Air M1 2020, 8GB RAM, 512GB SSD).

## Description of scripts
The script `community_model.ipynb` presents how the community assembly is simulated in silico. It first created a pool of species with random abilities and later combined all species in the same community to find survived species after their competition. Both essential functions and alternative resource consumption functions are included in the model. More details about the model can be found in the [manuscript]().

The script `comparision_of_functional_redundancy.ipynb` takes the microbial relative abundances, GCN (Gene Content Network) and PCN (Protein Content Network) and computed $\text{FR}_g$ and $\text{FR}_p$ for each protein function. Then we compare $\text{FR}_g$ and $\text{FR}_p$. 

## Example
We have simulated the result of one community assembly and saved the data to the "model_simulation_results.pickle". Here, the script `comparision_of_functional_redundancy.ipynb` direcly takes the simulated data from "community_model.ipynb", including the microbial relative abundances for survived species, GCN (Gene Content Network) and PCN (Protein Content Network). The script generated results and figures similar to the [paper]().

## License
This project is covered under the **MIT License**.