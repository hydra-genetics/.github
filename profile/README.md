![hydra-logo](hydra-genetics-project-logo.svg)

We are an organization/community with the goal of making [Snakemake](https://snakemake.readthedocs.io/en/stable/index.html) pipeline development easier and faster, and a bit more structured. 

We do this by providing [Snakemake modules](https://snakemake.readthedocs.io/en/stable/snakefiles/modularization.html#modules) that can be combined to create a complete analysis or included in already existing pipelines. All modules are subjected to extensive testing to make sure that new releases don't unexpectedly break existing pipeline or deviate from guidelines and best practices on how to write code.  

## Documentation
Please visit our [ReadTheDocs](https://hydra-genetics.readthedocs.io/en/latest/) for more information about using hydra-genetics.

## Pipelines built using Hydra-Genetics
A list of pipelines built with Hydra-Genetics [can be found here](https://github.com/hydra-genetics/hydra-genetics-pipelines).

## Repositories 

### Tools and examples

<table>
<tr>
<td width="25%" valign="top">

**[hydra-genetics](https://github.com/hydra-genetics/hydra-genetics)**

Command line interface to create new modules/pipelines or add new rules to an existing project. Provided libraries make it easier for people to extract information from sequencing files and generate [units.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/.tests/integration/units.tsv) ([schema definition](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/units.schema.yaml)) and [samples.tsv](https://github.com/hydra-genetics/prealignment/blob/develop/.tests/integration/samples.tsv) ([schema definition](https://github.com/hydra-genetics/prealignment/blob/develop/workflow/schemas/samples.schema.yaml)) tables.

</td>
<td width="25%" valign="top">

**[docker](https://github.com/hydra-genetics/docker)**

Collection of docker files with bioinformatic tools used to execute Snakemake with singularity. All dockers are automatically uploaded to [dockerhub](https://hub.docker.com/u/hydragenetics) (after being merged into master)

</td>
<td width="25%" valign="top">

**[profiles](https://github.com/hydra-genetics/profiles)**

Example of configuration profiles for executing Snakemake in various computing environments

</td>
<td width="25%" valign="top">

**[skills](https://github.com/hydra-genetics/hydra-genetics-skills)**

Collection of agent skills telling your AI agent how to write rules, create pipelines and modules according to Hydra-Genetics conventions.

</td>
</tr>
</table>

### Analysis modules

<table>
<tr>
<td width="25%" valign="top">

**[alignment](https://github.com/hydra-genetics/alignment)**

Snakemake module containing processing steps that are performed during sequence alignment.

</td>
<td width="25%" valign="top">

**[annotation](https://github.com/hydra-genetics/annotation)**

Collection of rules to annotate vcf files.

</td>
<td width="25%" valign="top">

**[biomarker](https://github.com/hydra-genetics/biomarker)**

Collection of rules used to calculate biomarkers like MSI, TMB and HRD.

</td>
<td width="25%" valign="top">

**[cnv_sv](https://github.com/hydra-genetics/cnv_sv)**

Collection of rules used to call structural variants

</td>
</tr>
<tr>
<td width="25%" valign="top">

**[compression](https://github.com/hydra-genetics/compression)**

Rules used to compress files

</td>
<td width="25%" valign="top">

**[filtering](https://github.com/hydra-genetics/filtering)**

Collection of variant filters

</td>
<td width="25%" valign="top">

**[fusions](https://github.com/hydra-genetics/fusions)**

Collection of fusion callers

</td>
<td width="25%" valign="top">

**[misc](https://github.com/hydra-genetics/misc)**

Snakemake module containing rules that are general and most likely will be used by multiple modules.

</td>
</tr>
<tr>
<td width="25%" valign="top">

**[mitochondrial](https://github.com/hydra-genetics/mitochondrial)**

Snakemake module for performing Mitochondrial short variant discovery

</td>
<td width="25%" valign="top">

**[parabricks](https://github.com/hydra-genetics/parabricks)**

Snakemake module containing an array of steps provided by the parabricks toolkit

</td>
<td width="25%" valign="top">

**[prealignment](https://github.com/hydra-genetics/prealignment)**

Snakemake module containing processing steps that are performed before sequence alignment.

</td>
<td width="25%" valign="top">

**[qc](https://github.com/hydra-genetics/qc)**

Collection of rules performing QC and generating reports.

</td>
</tr>
<tr>
<td width="25%" valign="top">

**[references](https://github.com/hydra-genetics/references)**

Collection of rules used to create references, panel of normals (PoN), and background filters.

</td>
<td width="25%" valign="top">

**[reports](https://github.com/hydra-genetics/reports)**

A module containing rules for various types of reports.

</td>
<td width="25%" valign="top">

**[sentieon](https://github.com/hydra-genetics/sentieon)**

Sentieon tools

</td>
<td width="25%" valign="top">

**[snv_indels](https://github.com/hydra-genetics/snv_indels)**

Collection of rules used to call snv and small indels

</td>
</tr>
</table>

### Environment
Repositories used to set up an environment for users using Windows or OSX, or any other system that doesn't support singularity.

#### [vagrant](https://github.com/hydra-genetics/vagrant)
Build script for a vagrant machine that can be used by Windows/OSX/Linux users to run Snakemake in combination with singularity, will not work for ARM CPU systems.

#### <s>[hydra-genetics/multipass](https://github.com/hydra-genetics/multipass)</s>