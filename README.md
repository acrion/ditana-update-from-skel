# ditana-update-from-skel

This package provides a Ditana-specific script to update a user’s home directory with files from `/etc/skel`.

## Description

`ditana-update-from-skel` is an expert-level tool designed primarily for Ditana GNU/Linux development purposes. It allows for the selective updating of a user’s home directory with files from `/etc/skel`, which may have been updated by package installations or system updates.

## Warning

This script is Ditana-specific and should only be used by experts who fully understand its implications. While it includes safeguards to prevent overwriting user-modified files, the generic copying from `/etc/skel` should be approached with caution.

## Purpose

The main purpose of this script is to facilitate testing and development of Arch packages that install files to `/etc/skel`. Normally, updates to `/etc/skel` do not affect existing user accounts. This script provides a way to selectively apply such updates without creating a new test user.

## Features

- Compares files in `/etc/skel` with the user’s home directory
- Identifies new files and changed files
- Preserves user-modified files (changed since Ditana installation)
- Offers an option to compare changed files before applying updates
- Allows the user to review and confirm changes before application

## Usage

To run the script:

```bash
/usr/bin/update-from-skel
```

The script will guide you through the process, showing which files will be updated or added, and giving you the option to compare changes before applying them.

## Note on Arch Package Guidelines

This script is designed for development and testing purposes. It’s important to note that Arch packages should never directly install files into existing user home directories. For more information, see the [Arch Package Guidelines](https://wiki.archlinux.org/title/Arch_package_guidelines).

## Installation

This package is not installed by default and is intended for development use:

```bash
sudo pacman -S ditana-update-from-skel
```

For more information about Ditana GNU/Linux development, visit [https://ditana.org](https://ditana.org)
