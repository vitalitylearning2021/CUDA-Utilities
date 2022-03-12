The repository contains useful resources for CUDA programmers.

## InputOutput

Load or save individual CPU or GPU arrays to `txt` files. 

### Dependencies

`VComplex` and `Utilities`.

### Allowed data types

All native C/C++ data types + CUDA's `float2` and `double2`.

### Routines

    template <class T>
    void saveGPUrealtxt(const T * d_in, const char *filename, const int M)    

Save an individual real GPU matrix pointed to by `d_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements.

    template <class T>
    void saveCPUrealtxt(const T * h_in, const char *filename, const int M)

Save an individual real CPU matrix pointed to by `h_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements.

    template <class T>
    void saveGPUcomplextxt(const T * d_in, const char *filename, const int M)

Save an individual complex GPU matrix pointed to by `d_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements. The complex type is from the *VComplex* library.

    void saveGPUcomplextxt(const float2 * d_in, const char *filename, const int M)

Save an individual complex, single precision GPU matrix pointed to by `d_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements. The complex type is CUDA's `float2`.

    void saveGPUcomplextxt(const double2 * d_in, const char *filename, const int M)

Save an individual complex, double precision GPU matrix pointed to by `d_in` to a `txt` file whose filename is `filename`. `M` is the number of array elements. The complex type is CUDA's `double2`.

    template <class T>
    T * loadCPUrealtxt(const char *filename, T * __restrict__ h_out, const int M)
    
Load an individual real CPU matrix pointed to by `h_out` from a `txt` file whose filename is `filename`. `M` is the number of array elements. 

    template <class T>
    T * loadGPUrealtxt(const char *filename, T * __restrict__ d_out, const int M)
    
Load an individual real GPU matrix pointed to by `d_out` from a `txt` file whose filename is `filename`. `M` is the number of array elements. 
 
