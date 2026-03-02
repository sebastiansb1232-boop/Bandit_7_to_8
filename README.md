# HackTheBox_Facts_Solve_Problem
It's just a simple solution to an easy problem.
# Facts | Hack The Box Writeup
> A comprehensive technical report for the "Facts" machine on the Hack The Box platform.

**Date:** March 1, 2026
**Author:** [Your Name]
**Category:** Linux
**Difficulty:** Easy
**Tags:** `#Pentesting` `#Enumeration` `#NetworkSecurity` `#HTB`

---

## Table of Contents
- [Overview](#overview)
- [Environment Setup](#environment-setup)
- [Enumeration](#enumeration)
- [Service Analysis](#service-analysis)

---

## Overview
[cite_start]The **Facts** machine is an "Easy" difficulty Linux instance. [cite_start]The primary focus of this laboratory involves web service enumeration, local DNS configuration, and the identification of potential attack vectors within a multi-port environment.

## Environment Setup

### 1. VPN Connection
[cite_start]The initial phase required establishing a secure tunnel to the Hack The Box infrastructure via OpenVPN. [cite_start]Upon successful connection, the target was identified at the IP address **10.129.244.96**.

### 2. Local DNS Configuration
To streamline web interaction, the target IP was mapped to a local hostname. [cite_start]This was achieved using the `tee` command with the `-a` (append) flag to ensure existing host data remained intact[cite: 1, 4]:

```bash
echo "10.129.244.96 facts.htb" | sudo tee -a /etc/hosts
