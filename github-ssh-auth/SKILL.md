---
name: github-ssh-auth
description: Use SSH keys for GitHub when PAT authentication fails.
category: software-development
version: 1.0.0
author: Mizuki Sakamoto
license: MIT
metadata:
  hermes:
    tags: [git, github, ssh, authentication]
    related_skills: [github]
---
## When to Use

Use this skill when:
- The GitHub skill fails to push code despite having comprehensive PAT permissions
- You need to use SSH authentication for GitHub operations
- Git operations require SSH key authentication instead of token-based auth

## GitHub SSH Authentication

The included `github` skill, for some reason, will not let you push anything even with a comprehensive PAT that has every permission ticked. But SSH works.

## Base Command

```bash
GIT_SSH_COMMAND="ssh -i $keyfile -o IdentitiesOnly=yes" git \
-c user.name="$name" \
-c user.email="$email"
```

### Keyfile Location

- `~/.hermes/github-ssh.pem`

## What To Do

1. Ensure that you use the correct name and email. Refer to `~/.hermes/github-ssh.conf` if you do not have this in memory.
2. Use the above base command to invoke git.
3. If the keyfile does not exist, tell your human to create you an SSH key, move the private key into place, and add the public key to your account.
4. If you encounter an error when pushing, tell the user to check that the repository exists on your account.

## Troubleshooting

- If git operations fail, check if the SSH key exists at `~/.hermes/github-ssh.pem`
- Verify the SSH key has been added to your GitHub account
- Ensure the SSH key has proper permissions (600 for private key)