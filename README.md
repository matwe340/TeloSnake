# TeloSnake - a wrapper pipeline to estimate telomere length from WGS data

Pipeline that takes WGS fastq or bam files as input and then returns the mean
telomere length as an output. Currently, two tools are included in this pipeline,
_telseq_ and _computel_.


## Installation

1. If you haven't yet, install [mamba](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html) or [micromamba](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html). ([conda](https://www.anaconda.com/) works as well, but I would recommend mamba/micromamba as they are a lot faster when installing)

2. Clone this repository and cd into it:

    ```bash
    git clone https://github.com/gmanthey/variant-calling.git
    cd variant-calling
    ```

3. Create a new environment from the environment specs file:

    Using mamba:
    ```bash
    mamba env create -f environment.yml
    ```

## Usage

1. Copy the `config.yml.template` file to `config.yml`

2. Adjust the following parameters in the `config.yml` file:
 - fastq_dir: Path to the (trimmed) fastq files per individual.
 - bam_dir: Path to the alignment (bam) files per individual.
 - genome_size: The estimated genome size of the organism you're looking at (in
 bp)
 - reference_assembly: Path + filename of the index file of the reference genome
 assembly. 
 - n_chr: An integer for the haploid number of chromosomes.
 - species: The name of the species; alternatively any project ID. 
 
