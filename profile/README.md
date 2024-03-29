# Hydra-Genetics

We are an organization/community with the goal of making [snakemake](https://snakemake.readthedocs.io/en/stable/index.html) pipeline development easier and faster, and a bit more structured. 

We do this by providing [snakemake modules](https://snakemake.readthedocs.io/en/stable/snakefiles/modularization.html#modules) that can be combined to create a complete analysis or included in already existing pipelines. All modules are subjected to extensive testing to make sure that new releases doesn't unexpectedly break existing pipeline or deviate from guidelines and best practices on how to write code. 

Current tests:
- [pycodestyle](https://pycodestyle.pycqa.org/en/latest/): (--max-line-length 130)
- [snakefmt](https://github.com/snakemake/snakefmt): (line-length 130)
- [snakemake](https://snakemake.readthedocs.io/en/stable/executing/cli.html?highlight=lint#UTILITIES) --lint: (line-length 130)
- [snakemake dry-run](https://snakemake.readthedocs.io/en/stable/executing/cli.html#useful-command-line-arguments)
- execution test with small dataset
- ~~execution: integration test witt complete dataset~~: planned to be implemented 

The small execution tests will make sure that the pipeline actually can be executed, i.e run and generate data. The integration test with complete data set will also evaluate the generated result to make sure that results does not change, if it's not deliberately.  

We also have a [development document](https://docs.google.com/document/d/1l2v1ItZBTDaI72vQPZcaQzxwVUao78XzIJvGASAAD9E/edit?usp=sharing) describing how a hydra-genetic pipeline/module should be structured, named and what a rule should contain.    

## ReadTheDocs
Please visit our [ReadTheDocs](https://hydra-genetics.readthedocs.io/en/latest/) for more information about using hydra-genetics.

## Pipelines built using Hydra-Genetics
A list of pipelines built with Hydra-Genetics can be found at [https://github.com/hydra-genetics/hydra-genetics-pipelines](https://github.com/hydra-genetics/hydra-genetics-pipelines).

## Repositories 
The current repositories can be divided into the following sections.

### Tools and examples

#### [hydra-genetics/tools](https://github.com/hydra-genetics/tools)
Command line interface to create new modules/pipelines or adding a new rule to a existing project. Provides libraries used to make it easier for people not used to [pandas](https://pandas.pydata.org/) to extract information from samples and units dataframes, these dataframes are generated from [units.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/.tests/integration/units.tsv) ([schema definition](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/units.schema.yaml)) and [samples.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/.tests/integration/samples.tsv) ([schema definition](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/samples.schema.yaml)) files  and used as input for hydra-genetics. 

#### [hydra-genetics/docker](https://github.com/hydra-genetics/docker)
Collection of docker files with bioinformatic tools used to execute snakemake with singularity. All dockers are automatically uploaded to [dockerhub](https://hub.docker.com/u/hydragenetics) (after being merged into master)

#### [hydra-genetics/profiles](https://github.com/hydra-genetics/profiles)
Example of configuration profiles for executing Snakemake in various computing environments

### Environment
Repositories used to setup an environment for users using windows or OSX, or any other system that doesn't support singularity.

#### [hydra-genetics/vagrant](https://github.com/hydra-genetics/vagrant)
Build script for a vagrant machine that can be used by Window/OSX/Linux user to run snakemake in combination with singularity, will not work for ARM cpu systems.

#### <s>[hydra-genetics/multipass](https://github.com/hydra-genetics/multipass)</s>

### Analysis modules

#### [hydra-genetics/alignment](https://github.com/hydra-genetics/alignment)
Snakemake module containing processing steps that are be performed during sequence alignment.

#### [hydra-genetics/annotation](https://github.com/hydra-genetics/annotation)
Collection of rules to annotate vcf files.

#### [hydra-genetics/biomarker](https://github.com/hydra-genetics/biomarker)
Collection of rules used to calculate biomarkers like MSI, TMB and HRD.

#### [hydra-genetics/cnv_sv](https://github.com/hydra-genetics/cnv_sv)
Collection of rules used to call structural variants

#### [hydra-genetics/compression](https://github.com/hydra-genetics/compression)
Rules used to compress files

#### [hydra-genetics/filtering](https://github.com/hydra-genetics/filtering)
Collection of variant filters

#### [hydra-genetics/fusions](https://github.com/hydra-genetics/fusions)
Collection of fusion callers

#### [hydra-genetics/misc](https://github.com/hydra-genetics/misc)
Module containing rules that are general and most likely will be used by multiple modules.

#### [hydra-genetics/mitochondrial](https://github.com/hydra-genetics/mitochondrial)
Snakemake module for performing Mitochondrial short variant discovery

#### [hydra-genetics/parabricks](https://github.com/hydra-genetics/parabricks)
Snakemake module containing an array of steps provided by the parabricks tookit

#### [hydra-genetics/prealignment](https://github.com/hydra-genetics/prealignment)
Snakemake module containing processing steps that are be performed before sequence alignment.

#### [hydra-genetics/qc](https://github.com/hydra-genetics/qc)
Collection of rules performing QC and generating reports.

#### [hydra-genetics/references](https://github.com/hydra-genetics/references)
Collection of rules used to create references, panel of normals (PoN), and background filters.

#### [hydra-genetics/sentieon](https://github.com/hydra-genetics/sentieon)
Sentieon tools

#### [hydra-genetics/snv_indels](https://github.com/hydra-genetics/snv_indels)
Collection of rules used to call snv and small indels









