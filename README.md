# `go-env`

Quick setup for an isolated Go development instance. Based on `conda` to faciliate usage on servers without `sudo` or root access or where global system installation of `go` is otherwise undesirable.

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

- at the time of writing, Go version 1.18 is not available in `conda`
