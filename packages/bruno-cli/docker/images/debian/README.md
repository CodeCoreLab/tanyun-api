# TanyunAPI CLI — Debian

Debian slim variant of the TanyunAPI CLI Docker image.

**Base image:** `node:24.22.3-slim`

## Building

```bash
docker build -t tanyun/cli:debian ./images/debian

# with specific TanyunAPI CLI version
docker build \
  --build-arg BRUNO_VERSION=3.3.0 \
  -t tanyun/cli:3.3.0-debian \
  ./images/debian
```

## Usage

```bash
# Run a collection
docker run -v $(pwd):/bruno tanyun/cli:debian run 

# with pinned version
docker run -v $(pwd):/bruno tanyun/cli:3.3.0-debian run 
```
