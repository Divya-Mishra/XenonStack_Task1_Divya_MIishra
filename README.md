# internsctl - Custom Linux Command

## Version: v0.1.0

---

## Table of Contents

1. [Overview](#overview)
2. [Installation](#installation)
3. [Usage](#usage)
   - [1. Manual Page](#1-manual-page)
   - [2. --help Option](#2---help-option)
   - [3. --version Option](#3---version-option)
4. [Section A](#section-a)
   - [1. Get CPU Information](#1-get-cpu-information)
   - [2. Get Memory Information](#2-get-memory-information)
5. [Section B - Part 1](#section-b---part-1)
   - [1. Create a New User](#1-create-a-new-user)
   - [2. List Regular Users](#2-list-regular-users)
6. [Section B - Part 2](#section-b---part-2)
   - [1. List Users with Sudo Permissions](#1-list-users-with-sudo-permissions)
7. [Section B - Part 3](#section-b---part-3)
   - [1. Get File Information](#1-get-file-information)


---

## Overview

internsctl is a custom Linux command designed to simplify various operations for server management. This document provides information on installation, usage, and available functionalities.

## Installation

To install internsctl, follow these steps:

1. Clone the repository:
   bash
   git clone https://github.com/Divya-Mishra/XenonStack_Task1_Divya_MIishra
   

2. Change into the internsctl directory:
   bash
   cd internsctl
   

3. Make the script executable:
   bash
   chmod +x internsctl.sh
   

4. Optionally, add the directory to your PATH for global accessibility:
   bash
   export PATH=$PATH:/path/to/internsctl
   

## Usage

### 1. Manual Page

bash
man internsctl


This command provides the full documentation and usage guidelines for internsctl.

### 2. --help Option

bash
internsctl --help


This command provides help and examples for the usage of internsctl.

### 3. --version Option

bash
internsctl --version


This command displays the version of internsctl.

---

## Section A

### 1. Get CPU Information

bash
internsctl cpu getinfo


This command provides CPU information similar to the output of the lscpu command.

### 2. Get Memory Information

bash
internsctl memory getinfo


This command provides memory information similar to the output of the free command.

---

## Section B - Part 1

### 1. Create a New User

bash
internsctl user create <username>


Creates a new user with login access to the Linux system and a home directory.

### 2. List Regular Users

bash
internsctl user list


Lists all regular users on the server.

---

## Section B - Part 2

### 1. List Users with Sudo Permissions

bash
internsctl user list --sudo-only


Lists all users with sudo permissions on the server.

---

## Section B - Part 3

### 1. Get File Information

bash
internsctl file getinfo [options] <file-name>


Options:
- --size, -s: Print file size.
- --permissions, -p: Print file permissions.
- --owner, -o: Print file owner.
- --last-modified, -m: Print last modified information.

Example:

bash
internsctl file getinfo --size --permissions hello.txt


Expected Output:


File: hello.txt
Access: -rw-r--r--
Size(B): 5448
Owner: xenonstack
Modify: 2020-10-07 20:34:44.616123431 +0530


---
