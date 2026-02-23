# Homelab Infrastructure



## Overview

This repository documents my personal homelab environment used to practice Linux system administration, containerization, networking, and secure remote access.



## Environment

- Ubuntu Server

- Docker

- Nextcloud (containerized)

- OSTicket (containerized)

- WireGuard VPN for secure remote access



## Architecture

Old Windows 10 machine repurposed as Ubuntu server

Docker used for service isolation

WireGuard configured for encrypted remote access

Local network segmentation for internal services



## Architecture Overview



[Remote User]

|

(Encrypted WireGuard Tunnel)

|

[Ubuntu Server (repurposed PC)]

|

+------------------------------+

| WireGuard VPN |

| Docker Engine |

+------------------------------+

|

+-------------------+--------------------+

| | |

[Nextcloud] \[Collabora] \[osTicket]

| |

[MariaDB: nextcloud-db] \[MariaDB: osticket-db]

|

[Persistent Volumes on Host Storage]





\*\*Notes\*\*

- WireGuard runs directly on the Ubuntu server to provide encrypted remote access.

- Application services are containerized using Docker.

- Each application has a dedicated MariaDB container for database isolation.

- Persistent volumes ensure data survives container restarts.

- The environment is designed to simulate small production-style infrastructure.



## Responsibilities

- Server installation and configuration

- Container deployment and management

- VPN setup and key management

- System updates and patching

- Troubleshooting and log analysis



## Goals

To simulate small production-like environments and strengthen skills in:

- Linux administration

- Networking fundamentals

- Infrastructure reliability

\- Secure remote access

