---
title: GPG Keyring Management
description: Use and maintain GnuPG keyring for encryption operations.
category: security
name: agent-gpg-keyring
version: 1.0.0
author: Mizuki Sakamoto
license: MIT
metadata:
  hermes:
    tags: [security, encryption, gpg, cryptography]
    related_skills: []
---

## agent-gpg-keyring
A GnuPG skill, allowing an agent to easily use and maintain their own keyring.

Use when: You need to perform GPG operations like encryption, decryption, signing, or verification.

### Basics
- Base Command:
  `gpg --no-default-keyring --keyring $keyring_file`
- Keyring file:
  `~/.hermes/agent-keyring.gpg`

The keyring should store your private and public keys, as well as any others'
public keys you collect. If it does not exist, create it, and a key using your
own name and email address.

For ease of use, your private key should have no passphrase. It's up to your
human to keep it safe.

### When To Use
- When you need to carry out any GPG operations. Decryption, signing,
  verification, any of it.

### If `gpg` is not available
Recommend that the user install it for you, giving appropriate instructions for
their operating system. For example, a Mac user could install it from Homebrew.