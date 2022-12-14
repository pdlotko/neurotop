Welcome to Topological Neuroscience Software.
This is a collection of programs for topological analysis of directed and not directed graphs. The input format is an incidence matrix. There are two formats of incidence matrices that are currently supported:
binary files. We assume here a binary files with a list of bool's.
.h5 files. To enable .h5 files, please uncomment the second line of file symmetric.cpp / directed.cpp. That line says: //#define H5Header. Note the special requirements of the structure of .h5 files which is currently imposed by the software. We assume that the .h5 file contains a fields named "matrix_0". To read a matix with a different name, please go to symmetric.cpp or directed.cpp file, and add the name of the matric to the call of a function 'readConnectionMatrix'. Note that for using this part, you need to have hdfp library installed and link it during the compilation.
The program compute standard, or directed flag complex of the graph given at the input and the Betti numbers of this complex (once the appropriate flag is set when calling the program). It also produce list of simplices when the appropriate flag is set.

To compile the program without HDF5 library, please call g++ -O3 symmetric.cpp and g++ -O3 directed.cpp. When compiling with HDF5 library please add -lhdf5 to the commands.
