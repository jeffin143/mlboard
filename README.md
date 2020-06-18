# mlboard
mlpack visualization tool

mlboard is a tool that allows you to log mlpack data in the format that the TensorBoard frontend can render in browsers.

mlboard is still in the development phase. You can track the development ideas [here](https://www.mlpack.org/gsocblog/Jeffin2020CBP.html)

### 0. Contents

  1. [Building mlboard from source](#1-building-mlboard-from-source)
  2. [Supported Summary Types](#2-supported-summary-types)
  3. [Usage](examples/getting-started.md)

### 1. Building the source code 

For mlboard to run, you have to install protobuf

- For Mac OS 

```
brew install protobuf
```

- For debian-based systems

```
sudo apt-get install libprotobuf-dev protobuf-compiler
```

would be sufficient. 

Make a build directory.  The directory can have any name, but 'build' is
sufficient.

```
    $ mkdir build
    $ cd build
```

The next step is to run CMake to configure the project.  Running CMake is the
equivalent to running `./configure` with autotools. 

```
    $ cmake ../
```

Once CMake is configured, building the library is as simple as typing 'make'.

```
    $ make
```

If you wish to install mlboard to `/usr/local/include/mlboard/`, `/usr/local/lib/`,
and `/usr/local/bin/`, make sure you have root privileges (or write permissions 
to those three directories), and simply type

```
    $ make install
```

and the mlboard headers are found in `/usr/local/include/mlpack/`.

### 2. Supported Summary types 

Following are the Summary you could log using mlboard:

- [Scaler Summary](examples/scaler.md)
- [Image Summary](examples/image.md)

Please glance [Getting started](examples/getting-started.md) to know more about how to use mlboard.