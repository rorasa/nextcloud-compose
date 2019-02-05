# Nextcloud-compose

Docker compose file to setup and start Nextcloud server anywhere.

## Usage

1. Make sure that Docker is setup and running,
2. Drop the docker-compose.yml at the root of the data directory,
3. Run docker-compose up to start the system,

## Drive permission issue

Nextcloud is designed to work in a directory that has the permission set to private (0770). Thus, while the external storage media such as a portable drive can be used as the system root, only the file systems that support the permission can be used.
This means that the drive to store Nextcloud data must be formatted as EXT, APFS, or NTFS. FAT32 and ExFAT are not supported and Nextcloud will declare permission error.

## Trusted domain

By default, the Nextcloud container only trusts the localhost domain, thus only accessible from the machine itself. To use the system over the network, the target domain (or ip address) must be added to the trusted_domain optionin config/config.php

