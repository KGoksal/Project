# Vagrant Configuration Summary

## Overview

This Vagrant configuration script sets up multiple virtual machines using VirtualBox. It utilizes the Hostmanager plugin to manage `/etc/hosts` entries for the VMs.

## VM Configurations

- **DB VM (db01)**
  - **Box**: CentOS Stream 9
  - **Hostname**: db01
  - **IP**: 192.168.56.55
  - **Memory**: 600 MB

- **Memcache VM (mc01)**
  - **Box**: CentOS Stream 9
  - **Hostname**: mc01
  - **IP**: 192.168.56.54
  - **Memory**: 600 MB

- **RabbitMQ VM (rmq01)**
  - **Box**: CentOS Stream 9
  - **Hostname**: rmq01
  - **IP**: 192.168.56.53
  - **Memory**: 600 MB

- **Tomcat VM (app01)**
  - **Box**: CentOS Stream 9
  - **Hostname**: app01
  - **IP**: 192.168.56.52
  - **Memory**: 800 MB

- **Nginx VM (web01)**
  - **Box**: Ubuntu Jammy64
  - **Hostname**: web01
  - **IP**: 192.168.56.51
  - **Memory**: 800 MB
  - **GUI Mode**: Enabled

## Purpose

The configuration ensures that each VM has specific settings for hostname, IP address, base box image, and memory allocation. Private network configuration allows VM communication, and VirtualBox settings customize the VM environment.
