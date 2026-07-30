# cloud9image

cloud9image is a lightweight, containerized version of the Cloud9 IDE. This image allows developers to quickly set up a consistent coding environment that can be easily deployed and shared.

## Quick Start

```sh
docker run -d \
  --name cloud9 \
  -p 8000:8000 \
  -e USERNAME=admin \
  -e PASSWORD=secret \
  -v /path/to/workspace:/workspace \
  gvoze32/cloud9:latest
```

Then open `http://localhost:8000` in your browser.

## Environment Variables

| Variable   | Description                          | Required |
| ---------- | ------------------------------------ | -------- |
| `USERNAME` | Cloud9 login username                | Yes      |
| `PASSWORD` | Cloud9 login password                | Yes      |
| `GITURL`   | Git repo URL to clone into workspace | No       |

## Volumes

| Path         | Description                       |
| ------------ | --------------------------------- |
| `/workspace` | Persistent workspace directory    |

## Ports

| Port   | Description         |
| ------ | ------------------- |
| `8000` | Cloud9 IDE web UI   |

## Versions

The Docker image supports the following versions:

- Ubuntu 20.04 (Focal Fossa)
- Ubuntu 22.04 (Jammy Jellyfish)
- Ubuntu 24.04 (Noble Numbat)

## DockerHub

This project is also available as a Docker image on DockerHub. You can pull the image using the following command, or browse all tags on [DockerHub](https://hub.docker.com/r/gvoze32/cloud9/tags):

```sh
docker pull gvoze32/cloud9:latest
```

**Available Tags:**

| Tag                    | Platforms   |
| ---------------------- | ----------- |
| `latest`               | linux/amd64 |
| `focal`, `amd64-focal` | linux/amd64 |
| `jammy`, `amd64-jammy` | linux/amd64 |
| `noble`, `amd64-noble` | linux/amd64 |
| `arm64v8-focal`        | linux/arm64 |
| `arm64v8-jammy`        | linux/arm64 |
| `arm64v8-noble`        | linux/arm64 |

Pull a specific variant with:

```sh
docker pull gvoze32/cloud9:<tag-name>
```
