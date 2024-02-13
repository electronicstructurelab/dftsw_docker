This repository contains a binary dftsw, Dockerfile, a basis set directory, and an example directory.


To building a container, simply run

`docker build -t dftsw-container .`


The container can be used interactively with "docker run -it"

`docker run -it --network=host  dftsw-container /bin/bash`


Once entering an interactive Docker environment, run the command below to activate the mpi module

`module load mpi`


Now, you can try running the code. Go to examples/water directory where you find a sample CLUSTER input file.

`cd examples/water`

Then run the dftsw code with

`mpirun -np 4 /home/fortran/dftsw_exe > print.log`


