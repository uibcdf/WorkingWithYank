# First tests with Yank

```
conda config --add channels omnia --add channels conda-forge
conda install yank
conda install yank-examples
```


### Sources:

http://getyank.org/latest/running.html


## Loading the environment

```
module load intel/compilers_and_libraries/2018.1.163 cmake/intel-2018.1.163_3.10.1 intel/mpi/2018.1.163 CUDA/intel-2018.1.163_9.0 conda/intel-2018.1.163_miniconda
source activate yank
```

## First commands

```
yank help
```

To get the available platforms:

```
yank platforms
```

#### Problem: CUDA is not visible

```
>yank platforms
Available OpenMM platforms:
    0 Reference
    1 CPU
    2 OpenCL
```


The problem is OpenMM does not support CUDA 9.1 yet:
https://github.com/pandegroup/openmm/issues/1969

This is the reason why CUDA 9.0 is now compiled with intel and will be the version loaded by default with conda.

## Examples
http://getyank.org/latest/examples/index.html
https://github.com/choderalab/yank-examples

```
/opt/apps/conda/intel-2018.1.163_miniconda/envs/yank/share/yank/examples/
```

## Locally

```
ssh node01
```

Tests

```
yank selftest


YANK Selftest
-------------
Yank Version 0.20.1 

Available OpenMM platforms:
    0 Reference
    1 CPU
    2 CUDA
    3 OpenCL



Valid OpenEye install not found
Not required, but please check install if you expected it


Checking GPU Computed Mode (if present)...
Found 2 NVIDIA GPUs in the following modes: [Default, Default]
These should all be in shared/Default mode for YANK to use them
YANK Selftest complete.
Thank you for using YANK!
```

Examples to test yank:



### Serial

### MPI

#### CPUs
#### GPUs

## Slurm

### Serial 1 node CPUS

### MPI

#### CPUs
#### GPUs


