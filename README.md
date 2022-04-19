# `go-env`

Quick setup for an isolated Go development instance ("virtual environment"). Based on `conda` to faciliate usage on servers without `sudo` or root access or where global system installation of `go` is otherwise undesirable.

# Setup

Setup with:

```
make install
```

- downloads and installs a fresh Miniconda instance in the current directory

- installs the Go SDK into the `conda` installation

Activate the `conda` Go environment with:

```
source conda/bin/activate
```

Then `cd` to your project dir to do work.

When finished, deactivate with:

```
conda deactivate
```

# Notes

- at the time of writing, [Go version 1.18](https://go.dev/blog/go1.18) is not available in `conda`

- `Makefile` recipes included for macOS and Linux

- this is not the officially supported method of installing and using Go, so if you do not know why you need to setup Go this way then you probably should not use these setup methods

- make sure you do not accidentally run a command like `go test ./...` in this directory where the `conda` Go installation is located! Put your Go projects in a subdir or another directory tree

# Resources & References

- `conda` package for Go: https://anaconda.org/conda-forge/go

- Go homepage: https://go.dev/

- Go official download page: https://go.dev/dl/
