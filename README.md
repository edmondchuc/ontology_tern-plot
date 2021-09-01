# TERN Plot Ontology

## NOTICE
This repository has been rebranded to [TERN Ontology](https://github.com/ternaustralia/ontology_tern). Contents of this repository is now archived.

Documentation online: https://ternaustralia.github.io/ontology_tern-plot/

This is the new Git repository for the TERN Plot ontology. It was originally hosted on Bitbucket in [TERNPlotData-ontology](https://bitbucket.org/terndatateam/ternplotdata-ontology/src/master/). Only the plot vocabulary was moved out of the former Git repository. 

See https://linkeddata.tern.org.au for our other Linked Data resources. 

The move to GitHub was motivated by the free GitHub Pages service to host the static contents of this repository. 

## Building the documentation
In the directory of `docs/`, run:

```
docker run --rm -it --name pylode -e ONTOLOGY_FILE=tern-plot.ttl -e OPTIONS="--css true" -v ${PWD}:/pyLODE/src/pylode/input edmondchuc/pylode
```

## Cleaning the TopBraid OWL2SHACL output

We use TopBraid Composer for the OWL2SHACL feature where a SHACL file containing shapes is generated from the OWL ontology. Running this docker container performs some post-processing on the SHACL file such as adding `sh:targetClass` to each `sh:NodeShape`. 

```
docker run --rm --name tbc-shacl-cleaner -e SHACL_FILE="tern-plot.shapes.ttl" -v ${PWD}:/home/input edmondchuc/tbc-shacl-cleaner
```

## Contact

**Edmond Chuc**  
e.chuc@uq.edu.au  
