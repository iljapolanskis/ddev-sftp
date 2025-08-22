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

## Configuration

You can customize the SFTP service by setting environment variables in your `.ddev/.env` file:

```bash
# SFTP port (host port mapping)
SFTP_PORT=2222

# SFTP credentials
SFTP_USERNAME=myuser
SFTP_PASSWORD=mypassword

# SFTP directory and user/group IDs
SFTP_UID=1001
SFTP_GID=1001
SFTP_DIR=upload

# Host path to mount
SFTP_HOST_PATH=../upload/sftp
```

After making changes, restart DDEV:

```bash
ddev restart
```

## Configuration Options

| Variable | Default | Description |
| -------- | ------- | ----------- |
| `SFTP_PORT` | `2222` | Host port for SFTP access |
| `SFTP_USERNAME` | `sftp` | SFTP username |
| `SFTP_PASSWORD` | `sftp` | SFTP password |
| `SFTP_UID` | `1001` | User ID for SFTP user |
| `SFTP_GID` | `1001` | Group ID for SFTP user |
| `SFTP_DIR` | `upload` | Directory name inside SFTP home |
| `SFTP_HOST_PATH` | `../upload/sftp` | Host path to mount as SFTP directory |

## Connecting to SFTP

Once configured, you can connect to the SFTP service using:
- **Host**: `localhost` (or your DDEV hostname)
- **Port**: Value of `SFTP_PORT` (default: 2222)
- **Username**: Value of `SFTP_USERNAME` (default: sftp)
- **Password**: Value of `SFTP_PASSWORD` (default: sftp)

## Credits

**Contributed and maintained by [@iljapolanskis](https://github.com/iljapolanskis)**
