# Single VPS Host Instructions

![developer](https://img.shields.io/badge/Developed%20By%20%3A-Giorgio%20Tassinari-red)

## Description

I'm using this repo to keep the necessary setup files needed for my VPS for running any of my side projects. This assumes all my side projects are built as docker images and uploaded to my AWS ECR account.

## Setup

The setup.sh script is meant to work on a Digital Ocean Ubuntu 23.10 x64 VM.

1. `ssh root@MACHINE_IP`
1. `aws configure`
1. `cd /root`
1. `git clone https://github.com/webdevcody/single-vps-host`
1. `cd single-vps-host`
1. place certs in `./certs/${SERVICE_NAME}.pem`
1. place keys in `./private/${SERVICE_NAME}.pem`
1. `./setup.sh`
1. `docker compose up -d`

## Services

- [x] Nginx
- [x] Certbot
- [x] Docker
- [x] Docker Compose
- [x] AWS CLI
- [x] AWS ECR Login
- [x] AWS ECR Pull
- [x] AWS ECR Push
- [x] AWS ECR Logout
