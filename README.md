# Running nf-core/sarek with Nextflow

This directory contains notes on using the **nf-core/sarek** pipeline for germline and somatic variant calling with Nextflow.

## Requirements

- Nextflow installed and available in `PATH`
- Docker or Singularity (recommended)
- Internet connection (for first-time download of the pipeline and containers)

## 1. Pull the nf-core/sarek pipeline

Download the specified version of the pipeline into your local Nextflow assets cache:

```bash
nextflow pull nf-core/sarek
````

You can check available versions or update later with the same command.

## 2. List available pipelines

To see which pipelines are currently available in your Nextflow cache:

```bash
nextflow list
```

This will include `nf-core/sarek` once it has been pulled successfully.

## 3. Inspect cached pipeline files

Nextflow stores pulled pipelines under `$NXF_HOME/assets/` (or `~/.nextflow/assets/` by default).
You can inspect the structure of the cached `nf-core/sarek` code with:

```bash
tree -L 2 $NXF_HOME/assets/
```

This is useful to see where Nextflow keeps the pipeline source.

## 4. Create a local symlink to the Sarek pipeline

If you want a convenient local handle (e.g. to inspect or customize the pipeline code), create a symbolic link:

```bash
ln -s $NXF_HOME/assets/nf-core/sarek/ pipelines
```

Now you can access the Sarek code under the `pipelines/` directory, for example:

```bash
cd pipelines
ls
```

From here, you can read the documentation, inspect `nextflow.config`, and study how nf-core structures a production-grade Nextflow pipeline.

```
::contentReference[oaicite:0]{index=0}
```
