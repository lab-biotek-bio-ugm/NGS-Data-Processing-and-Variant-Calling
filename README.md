# NGS-Data-Processing-and-Variant-Calling

[<a href="https://codespaces.new/lab-biotek-bio-ugm/NGS-Data-Processing-and-Variant-Calling"><img src="https://github.com/codespaces/badge.svg" alt="Open in GitHub Codespaces" height="24"></a> <a href="https://colab.research.google.com/github/lab-biotek-bio-ugm/NGS-Data-Processing-and-Variant-Calling/blob/main/Modules-collab.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" height="24"></a> <a href="https://mybinder.org/v2/gh/lab-biotek-bio-ugm/NGS-Data-Processing-and-Variant-Calling/HEAD"><img src="https://mybinder.org/badge_logo.svg" alt="Open in Binder" height="24"></a>

**Bahasa Indonesia**

Alur kerja pemrosesan data NGS dan pemanggilan variasi sederhana.
Menggunakan `bwa`, `samtools`, `bcftools` dan visualisasi dengan `IGV`.

**English**

A workflow for NGS data processing and simple variant calling.
Uses `bwa`, `samtools`, `bcftools`, and visualization with `IGV`.

# Quick Start
- Create the conda environment by:

    ```bash
    conda env create -f environment.yml
    ```

- Activate the environment by typing:

    ```bash
    conda activate variant_calling
    ```

- Run jupyter by typing:

    ```bash
    jupyter lab --ServerApp.allow_origin='*'
    ```

## Run in Google Colab

You can open the notebook in Google Colab using the buttons above. Replace `OWNER`, `REPO`, and `BRANCH` in the badge link with your GitHub user/org, repository name, and branch (for example `main`) so Colab can fetch the notebook file from GitHub.

A minimal Colab setup cell (run in the first notebook cell) to install common Python dependencies used by the notebooks:

```bash
# Upgrade pip
!pip install -q --upgrade pip

# Install common Python packages used by the notebooks
!pip install -q pandas numpy matplotlib seaborn ipywidgets pysam

# Try installing IGV Jupyter integration (may have different package names)
!pip install -q igv-jupyter || true

# Snakemake and many CLI bioinformatics tools are packaged for conda/bioconda
# and may not install cleanly on Colab. For the full workflow (bwa/samtools/bcftools),
# create the conda environment locally with:
#     conda env create -f environment.yml
```

Note: several command-line bioinformatics tools (`bwa`, `samtools`, `bcftools`) are provided via bioconda and are not available via pip. They will not be available in Colab without using conda or custom apt packages. If you need the full workflow, run it locally using the provided `environment.yml`.
