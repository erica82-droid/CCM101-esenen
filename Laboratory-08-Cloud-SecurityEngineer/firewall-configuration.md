# Firewall Configuration

## 1. Allow SSH Access

The following command allows incoming SSH connections so administrators can remotely manage the server.

```bash
sudo ufw allow ssh
```

## 2. Configure the Default Deny Policy

These commands block incoming traffic by default while allowing outgoing traffic.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

## 3. Allow Port 8080

This command allows incoming TCP traffic on port 8080 for the Nginx web application.

```bash
sudo ufw allow 8080/tcp
```

## 4. Enable the Firewall

The following command activates the UFW firewall.

```bash
sudo ufw enable
```

To verify the firewall configuration, use:

```bash
sudo ufw status verbose
sudo ufw status numbered
```

## 5. SSH Security Warning

If `sudo ufw enable` is executed before `sudo ufw allow ssh`, incoming SSH connections may be blocked by the default deny policy, potentially locking administrators out of a remote server.

## 6. Security Summary

The firewall configuration follows the Default Deny principle by blocking incoming connections unless they are explicitly allowed. SSH access is permitted for administration, and TCP port 8080 is allowed for the web application.
