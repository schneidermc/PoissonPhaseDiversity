# PoissonPhaseDiversity


### Create conda environment

`conda env create -f environment.yml`

`conda activate cuda-pd`


### Compile CUDA libraries

Navigate into subfolder `cuda`. Compile the `c_functions.cu` file:

`nvcc -shared -Xcompiler -fPIC -diag-suppress=177 -o c_functions.so c_functions.cu -lcudart -lcufft -lcublas`

This will compile the file, link CUDA runtime, cuFFT and cuBLAS, and suppress warnings.


