---
layout: default
title: FAQ
parent: Home
nav_order: 10
---

## Frequently Asked Questions

This is a list of the most common questions or issues that our users encounter.

### Setup SSH access to your workspace

- Generate an ssh key pair using `ssh-keygen -t ed25519 -C "<comment>"`.
- Create an `authorized_keys` file under `~/.ssh/` in your workspace.
- Add your **public** ssh key to the `authorized_keys` file.
- Acquire the public IP address of your workspace by running `curl ifconfig.me` in a terminal.
- Attempt to connect to your workspace from your local machine using your private key, workspace user, and IP address (e.g `ssh -i path-to-private-key user-name@ip-address`).
- [Optional] Create an alias for connecting to your workspace by adding an entry to a `config` file under `~/.ssh/` in your local machine.

```text
Host <alias>
    HostName <remote-ip>
    User <remote-user>
```