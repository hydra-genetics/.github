# Hydra-Genetics

We are an organization/community with the goal of making [snakemake](https://snakemake.readthedocs.io/en/stable/index.html) pipeline development easier and faster, and a bit more structured. 

We do this by providing [snakemake modules](https://snakemake.readthedocs.io/en/stable/snakefiles/modularization.html#modules) that can be combined to create a complete analysis or included in already existing pipelines. All modules are subjected to extensive testing to make sure that new releases doesn't unexpectedly break existing pipeline or deviate from guidelines and best practices on how to write code. Current tests:
- [pycodestyle](https://pycodestyle.pycqa.org/en/latest/): (--max-line-length 130)
- [snakefmt](https://github.com/snakemake/snakefmt): (line-length 130)
- [snakemake](https://snakemake.readthedocs.io/en/stable/executing/cli.html?highlight=lint#UTILITIES) --lint: (line-length 130)
- [snakemake dry-run](https://snakemake.readthedocs.io/en/stable/executing/cli.html#useful-command-line-arguments)
- execution test with small dataset
- ~~execution: integration test witt complete dataset~~: planned to be implemented 

The small execution tests will make sure that the pipeline actually can be executed, i.e run and generate data.  

We also have a [development document](https://docs.google.com/document/d/1l2v1ItZBTDaI72vQPZcaQzxwVUao78XzIJvGASAAD9E/edit?usp=sharing) describing how a hydra-genetic pipeline/module should be structured, named and what a rule should contain.    

## Repositories 
The current repositories can be divided into the following sections

### Tools and examples

#### [hydra-genetics/tools](https://github.com/hydra-genetics/tools)
Command line interface to create new modules/pipelines or adding a new rule to a existing project. Provides libraries used to make it easier for people not used to pandas to extract information from samples and units dataframes, dataframes generate from [units.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/units.schema.yaml) and [samples.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/samples.schema.yaml) files which are used as input. 

#### [hydra-genetics/docker](https://github.com/hydra-genetics/docker)
Collection of docker files with bioinformatic tools used to execute snakemake with singularity, all dockers are automatically uploaded to [dockerhub](https://hub.docker.com/u/hydragenetics) (after being merged into master)

#### [hydra-genetics/profiles](https://github.com/hydra-genetics/profiles)
Example of configuration profiles for executing Snakemake in various computing environments


### Analysis modules

#### [hydra-genetics/prealignment](https://github.com/hydra-genetics/prealignment)
#### [hydra-genetics/alignment](https://github.com/hydra-genetics/alignment)
#### [hydra-genetics/snv_indels](https://github.com/hydra-genetics/snv_indels)
#### [hydra-genetics/annotation](https://github.com/hydra-genetics/annotation)
#### [hydra-genetics/cv_sv](https://github.com/hydra-genetics/cv_sv)
#### [hydra-genetics/biomarkers](https://github.com/hydra-genetics/biomarkers)
#### [hydra-genetics/qc](https://github.com/hydra-genetics/qc)
#### [hydra-genetics/misc](https://github.com/hydra-genetics/misc)
#### [hydra-genetics/references](https://github.com/hydra-genetics/references)





