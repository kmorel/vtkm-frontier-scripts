This repository contains the Spack configuration required to compile VTK-m
on Frontier as long as scripts to enable the configuration and compile the
code. This repository also has submodules for Spack itself and the E4S
configuration of Spack. Thus, when you check out this repository, you need
to initialize and update the submodules.

``` bash
git clone https://github.com/kmorel/vtkm-frontier-scripts.git
cd vtkm-frontier-scripts
git submodule update --depth=100 --init
```

To set up and load the Spack environment, simply source the
`setup-spack.sh` script.

``` sh
. ./setup-spack.sh
```

To compile VTK-m, run the `make-vtkm.sh` script. You do not have to source
`setup-spack.sh` before running `make-vtkm.sh`, but you will have to source
it before using it. You can load VTK-m into your environment with

``` bash
spack load vtk-m
```
