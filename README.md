[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/iljapolanskis/ddev-sftp/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/iljapolanskis/ddev-sftp/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/iljapolanskis/ddev-sftp)](https://github.com/iljapolanskis/ddev-sftp/commits)
[![release](https://img.shields.io/github/v/release/iljapolanskis/ddev-sftp)](https://github.com/iljapolanskis/ddev-sftp/releases/latest)

# DDEV Sftp

## Overview

This add-on integrates Sftp into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get iljapolanskis/ddev-sftp
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Sftp |
| `ddev logs -s sftp` | Check Sftp logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.sftp --sftp-docker-image="busybox:stable"
ddev add-on get iljapolanskis/ddev-sftp
ddev restart
```

Make sure to commit the `.ddev/.env.sftp` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `SFTP_DOCKER_IMAGE` | `--sftp-docker-image` | `busybox:stable` |

## Credits

**Contributed and maintained by [@iljapolanskis](https://github.com/iljapolanskis)**
