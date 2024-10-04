# Pell
---

# Pell CLI Installation Guide

> **Note:** This document is in a draft stage. The content may change as the project evolves. For the most up-to-date information, always refer to the latest version or contact the team.

## Software Requirements

- **Docker**: Ensure Docker is installed. [Installation guide](https://docs.docker.com/get-docker/).
- **Docker Compose**: Ensure Docker Compose is also installed and configured. [Installation guide](https://docs.docker.com/compose/install/).
- **Linux Environment**: Pell Node Operator SDK is supported on Linux. Make sure you have a Linux environment such as Docker.

If you choose to install `pell-cli` using Go, ensure Go version 1.21 or higher is installed. [Installation guide](https://go.dev/doc/install).

## CLI Installation

### 1. Install CLI using Binary

To download and install the latest release:

```bash
curl -sSfL https://raw.githubusercontent.com/0xPellNetwork/pell-cli/master/scripts/install.sh | sh -s
```

The binary will be installed in the `~/bin` directory. Add it to your system PATH:

```bash
export PATH=$PATH:~/bin
```

### 2. Install CLI in a Custom Location

To install the binary in a custom directory:

```bash
curl -sSfL https://raw.githubusercontent.com/0xPellNetwork/pell-cli/master/scripts/install.sh | sh -s -- -b <custom_location>
```

### 3. Install CLI Using Go

Install the `pell-cli` using Go:

```bash
go install github.com/0xPellNetwork/pell-cli/cmd/pell-cli@latest
```

To ensure `GOBIN` is in your PATH, check:

```bash
echo $GOBIN
```

If nothing is printed, add the following to your `$HOME/.profile`:

```bash
export GOBIN=$GOPATH/bin
export PATH=$GOBIN:$PATH
```

Apply the changes by running:

```bash
source $HOME/.profile
```

### 4. Install CLI from Source

Make sure Go (version 1.21 or higher) is installed. Then, follow these steps:

```bash
git clone https://github.com/0xPellNetwork/pell-cli.git
cd pell-cli
mkdir -p build
go build -o build/pellcmd cmd/pell/main.go
```

Alternatively, if you have `make` installed:

```bash
git clone https://github.com/0xPellNetwork/pell-cli.git
cd pell-cli
make build2
```

The executable will be in the `build` folder.

---
