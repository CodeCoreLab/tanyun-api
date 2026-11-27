# TanyunAPI CLI — Alpine

Alpine Linux variant of the TanyunAPI CLI Docker image.

**Base image:** `node:24.22.3-alpine`

## Building

```bash
docker build -t tanyun/cli:alpine ./images/alpine

# with specific TanyunAPI CLI version
docker build \
  --build-arg BRUNO_VERSION=3.3.0 \
  -t tanyun/cli:3.3.0-alpine \
  ./images/alpine
```

## Usage

```bash
# Run a collection
docker run -v $(pwd):/bruno tanyun/cli:alpine run

# with pinned version
docker run -v $(pwd):/bruno tanyun/cli:3.3.0-alpine run
```
