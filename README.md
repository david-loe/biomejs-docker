# Docker images for Biome

This repository contain the source code for building the official Docker images
for Biome.

Supported architectures: `amd64`, `arm64`

## Supported tags

Docker images are available for all versions of Biome starting from `1.7.0`.

Images are tagged with the following format:

```sh
ghcr.io/biomejs/biome:{major}
ghcr.io/biomejs/biome:{major}.{minor}
ghcr.io/biomejs/biome:{major}.{minor}.{patch}
```

### Examples
- `ghcr.io/biomejs/biome:1`
- `ghcr.io/biomejs/biome:1.9`
- `ghcr.io/biomejs/biome:1.9.4`
- `ghcr.io/biomejs/biome:latest`

## Usage

The default working directory is set to `/code` in the container.

```sh
# Check files
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 check
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 check --write

# Lint files
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 lint
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 lint --write

# Format files
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 format
docker run -v $(pwd):/code ghcr.io/biomejs/biome:1.9.4 format --write
```

## License

This project is licensed under the [MIT License](LICENSE.md).