# TERN Plot Ontology

This is the new Git repository for the TERN Plot ontology. It was originally hosted on Bitbucket in [TERNPlotData-ontology](https://bitbucket.org/terndatateam/ternplotdata-ontology/src/master/). Only the plot vocabulary was moved out of the former Git repository. 

See https://linkeddata.tern.org.au for our other Linked Data resources. 

The move to GitHub was motivated by the free GitHub Pages service to host the static contents of this repository. 

## Building the documentation
In the directory of `docs/`, run:

```
docker run --rm -it --name pylode -e ONTOLOGY_FILE=tern-plot.ttl -e OPTIONS="--css true" -v ${PWD}:/pyLODE/src/pylode/input edmondchuc/pylode
```

## Contact

**Edmond Chuc**  
e.chuc@uq.edu.au  