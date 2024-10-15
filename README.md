# OpenSSH Server Hardening Checklist

Hardening an OpenSSH server is crucial for securing remote access to your Linux system. Below is a comprehensive checklist to help you secure your OpenSSH server.

## Checklist

- [ ] **Keep OpenSSH Up to Date:**
  - Regularly update the OpenSSH server to the latest version to patch known vulnerabilities.
  - Keep your operating system up to date as well.

- [ ] **Implement Two-Factor Authentication (2FA):**
  - Implement two-factor authentication for an extra layer of security.

- [ ] **Change Default Port:**
  - Consider changing the default SSH port (usually 22) to a non-standard port to deter automated attacks.

- [ ] **Configure SSH Idle Timeout:**
  - Set an idle session timeout to automatically log out inactive users.

- [ ] **Enable SSH Logging:**
  - Enable SSH session logging and regularly review the logs for security incidents.

- [ ] **Use SSH Keys with Passphrases:**
  - Disable password-based authentication and use SSH keys for authentication.
  - Generate strong SSH keys (at least 2048 bits) and protect the private key with a passphrase.

- [ ] **Implement Firewall Rules:**
  - Use firewall rules to restrict SSH access to trusted IP addresses or networks.

- [ ] **Monitor SSH Logs:**
  - Regularly review SSH logs for suspicious activity.
  - Consider using tools like `Fail2ban` or `DenyHosts` for blocking repeated failed login attempts.

- [ ] **Disable Password-Based SSH Login:**
  - Disable password-based authentication in your SSH server configuration (`PasswordAuthentication no`).

- [ ] **Disable Unused SSH Features (i.e., SSHv1):**
  - Disable any unused or outdated SSH features in the SSH server configuration.

- [ ] **Regularly Audit SSH Server Configuration:**
  - Perform regular security audits of your SSH server configuration to identify and fix vulnerabilities.

- [ ] **Disable User SSH Passwordless Connection Requests:**
  - Ensure that users cannot establish passwordless SSH connections to the server.

- [ ] **Disable SSH Root Logins:**
  - Disable direct root logins in the SSH server configuration (`PermitRootLogin no`).

- [ ] **Configure a Limit for Password Attempts:**
  - Configure a limit for the number of password login attempts to prevent brute-force attacks.

- [ ] **Disable X11 Forwarding:**
  - Unless needed, consider disabling X11 forwarding in the SSH server configuration (`X11Forwarding no`).

- [ ] **Use Public Key Authentication:**
  - Promote the use of public key authentication among users.

- [ ] **Use SSH Connection Limits:**
  - Limit the number of concurrent SSH connections to reduce the risk of DoS attacks.

- [ ] **Use Strong Host Keys:**
  - Ensure that your SSH server uses strong host keys (RSA, ECDSA, or Ed25519).

- [ ] **Regularly Rotate SSH Keys:**
  - Implement a policy for regularly rotating SSH keys.

- [ ] **Implement Fail2Ban or Similar:**
  - Use tools like `Fail2Ban` to monitor logs and block IP addresses after a specified number of failed login attempts.

- [ ] **Use a VPN for SSH Access:**
  - Consider using a Virtual Private Network (VPN) for added security when accessing SSH.

- [ ] **Restrict User Access:**
  - Implement user roles and restrict access based on the principle of least privilege.

- [ ] **Audit SSH User Access:**
  - Regularly review the list of users with SSH access and remove any that are no longer needed.

- [ ] **Disable SSH Protocol Version 1:**
  - Ensure that SSH Protocol version 1 is disabled as it has known vulnerabilities.

- [ ] **Use Strong Encryption Algorithms:**
  - Ensure that the SSH server is configured to use strong encryption algorithms to protect data in transit.
