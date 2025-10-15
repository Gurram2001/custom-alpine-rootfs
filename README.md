# Custom Alpine Docker Image with GitHub Actions CI

This repo shows how to build a minimal Docker image using Alpine Rootfs and automate builds with GitHub Actions.

## Steps

1. Download official Alpine Rootfs latest from website:
   `wget https://dl-cdn.alpinelinux.org/alpine/v3.22/releases/x86_64/alpine-minirootfs-3.22.2-x86_64.tar.gz`

2. Place Dockerfile and .tar.gz in repo root.

3. Build locally:
   `docker build -t custom-alpine:latest .`
4. Check with  `docker run -it custom-alpine:latest`
5. Once you enter shell. Check with ` cat /etc/os-release`
<img width="851" height="245" alt="image" src="https://github.com/user-attachments/assets/3938326a-fab7-486e-9d05-537bf13f6eb3" />

6. Clone this repo, once you completed manual process with CI/CD: On push to main, image is built and pushed automatically!

## Customization

- Edit Dockerfile to add packages via RUN apk add --no-cache package
- Update workflow for tags or registry as needed

