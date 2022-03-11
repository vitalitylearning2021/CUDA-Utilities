The repository contains useful resources for CUDA programmers.

# InputOutput

Load or save individual CPU or GPU arrays to `txt` files. Allowed data types: `

## Dependencies

`BBComplex` and `Utilities`.

## Allowed data types

All native C/C++ data types + `float2` and `double2`.

    void saveGPUrealtxt(const T *, const char *, const int);
    
Save an individual SAVE INDIVIDUAL REAL GPU MATRIX TO txt FILE

template <class T>
void saveCPUrealtxt(const T *, const char *, const int);

template <class T>
void saveGPUcomplextxt(const T *, const char *, const int);

void saveGPUcomplextxt(const double2 *, const char *, const int);

template <class T>
T * loadCPUrealtxt(const char *, T * __restrict__, const int);

template <class T>
T * loadGPUrealtxt(const char *, T * __restrict__, const int);
