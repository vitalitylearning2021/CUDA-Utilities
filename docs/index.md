The repository contains useful resources for CUDA programmers.

## InputOutput

Load or save individual CPU or GPU arrays to `txt` files. 

### Dependencies

`BBComplex` and `Utilities`.

### Allowed data types

All native C/C++ data types + `float2` and `double2`.

### Routines

    template <class T>
    void saveGPUrealtxt(const T * d_in, const char *filename, const int M)    

Save an individual real GPU matrix pointed to by `d_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements.

template <class T>
void saveCPUrealtxt(const T *, const char *, const int);

template <class T>
void saveGPUcomplextxt(const T *, const char *, const int);

void saveGPUcomplextxt(const double2 *, const char *, const int);

template <class T>
T * loadCPUrealtxt(const char *, T * __restrict__, const int);

template <class T>
T * loadGPUrealtxt(const char *, T * __restrict__, const int);
