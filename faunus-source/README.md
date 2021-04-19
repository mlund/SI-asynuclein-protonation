## Monte Carlo Simulation Software

For optionally running simulations, [Faunus](https://github.com/mlund/faunus) must be build using a C++ compiler.

``` bash
    cd faunus-source/
    unzip faunus-075bf8de.zip 
    patch CMakeLists.txt patch1-eigen.diff # apply patch due to URL change of dependency
    cmake . -DCMAKE_BUILD_TYPE=Release
    make faunus -j
```

The Faunus revision included here is close to v2.4.x and you may be able to use that instead.

## Faunus executables

As an alternative to the C++ source compilation above, we provide a few pre-compiled executables.
Use at your own risk.

Executable            | Operating system
--------------------- | ------------------------------------
`faunus-macos-arm64`  | macOS M1
`faunus-macos-x86`    | macOS intel (and M1 through rosetta)
