FROM node:24.22.3-slim

LABEL maintainer="TanyunAPI <https://github.com/CodeCoreLab/tanyun-api>"

ARG BRUNO_VERSION
ENV BRUNO_VERSION=${BRUNO_VERSION}

LABEL org.opencontainers.image.source="https://github.com/CodeCoreLab/tanyun-api"
LABEL org.opencontainers.image.description="TanyunAPI CLI - Open source IDE for exploring and testing APIs"
LABEL org.opencontainers.image.licenses="MIT"
LABEL org.opencontainers.image.title="TanyunAPI CLI"
LABEL org.opencontainers.image.version="${BRUNO_VERSION}"
LABEL org.opencontainers.image.url="https://github.com/CodeCoreLab/tanyun-api"
LABEL org.opencontainers.image.documentation="https://github.com/CodeCoreLab/tanyun-api#cli"

ENV LC_ALL="en_US.UTF-8" \
    LANG="en_US.UTF-8" \
    LANGUAGE="en_US.UTF-8"

# If BRUNO_VERSION is provided, validate it is a valid semver before installing
RUN if [ -n "$BRUNO_VERSION" ]; then \
        if ! echo "$BRUNO_VERSION" | grep -qE "^[0-9]+\.[0-9]+\.[0-9]+$"; then \
            echo "\033[0;31mA valid semver TanyunAPI CLI version is required in the BRUNO_VERSION build-arg (e.g. 1.16.0)\033[0m"; \
            exit 1; \
        fi; \
    fi && \
    npm install -g @usebruno/cli${BRUNO_VERSION:+@${BRUNO_VERSION}}

WORKDIR /bruno

USER node

ENTRYPOINT ["bru"]
CMD []
