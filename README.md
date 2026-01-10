# github-actions

![Static Badge](https://img.shields.io/badge/Kubernetes-blue?style=social&logo=Kubernetes) ![Static Badge](https://img.shields.io/badge/GitHub_Actions-blue?style=social&logo=githubactions)

This repository contains examples for building and deploying to Dev and Prod environments using GitHub Actions to a K8s cluster.

## This repository has examples of GitHub Workflows for:

- `.github/workflows/`
  - `dev.yaml`
    - Automatically build and deploy into Dev when a PR is open.
  - `prod.yaml`
    - Automatically build and deploy into Dev when a PR is approved.

## It also contains examples of Kubernetes resources:

- `nginx/`
  - Nginx with PHP and volume (path) mounted from the host.
  - `docker/Dockerfile`
    - Container image build configuration.
  - `nginx-combined.yaml`
    - Combined manifests
      - Namespace
      - Deployment
      - Service
      - Ingress

- `kuma/`
  - UptimeKuma with Persistent Volume.
  - `docker/Dockerfile`
    - Container image build configuration.
  - `kuma-combined.yaml`
    - Combined manifests:
      - Namespace
      - Persistent Volume
      - Persistent Volume Claim
      - Deployment
      - Service
      - Ingress

- `runner/`
  - GitHub Actions Runnel with Privileged Security context and Repository Secrets.
  - `docker/Dockerfile`
    - Container image build configuration.
  - `runner-combined.yaml`
    - Combined manifests
      - Namespace
      - Deployment

- `tunnel/`
  - Cloudflare Tunnel with Repository Secret.
  - `docker/Dockerfile`
    - Container image build configuration.
  - `tunnel-combined.yaml`
    - Combined manifests
      - Namespace
      - Deployment

## For more information, check out:

- https://dft.wiki/?p=1372
  - Kubernetes Cheat Sheet
- https://dft.wiki/?p=3122
  - Kubernetes Manifests Demo
- https://dft.wiki/?p=1435
  - Kubernetes Persistent Volumes
