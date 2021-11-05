# Hydra-Genetics

We are an organization/community with the goal of making snakemake pipeline development easier and faster, and a bit more structured. 

We do this by providing snakemake modules that can be combined to create a complete analysis or included in already existing pipelines. All modules are subjected to extensive testing to make sure that new releases doesn't unexpectedly break existing pipeline or deviate from guidelines and best practices on how to write code. Current tests:
- pycodestyle: (--max-line-length 130)
- snakefmt: (line-length 130)
- snakemake --lint: (line-length 130)
- snakemake dry-run
- snakemake: integration test with small dataset
- ~~snakemake: integration test witt complete dataset~~: planned to be implemented 

## Repositories 
The current repositories can be divided into the following sections
