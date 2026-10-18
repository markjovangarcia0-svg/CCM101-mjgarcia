# Firewall Configuration

## Mission 8: The Cloud Security Engineer

This document records the UFW commands used to secure an Ubuntu server hosting an Nginx web application.

## Step 1: Allow SSH

```bash
sudo ufw allow ssh
```

This rule allows SSH connections on port 22 for remote administration.

## Step 2: Configure Default Firewall Policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands deny incoming connections by default while allowing outgoing traffic.

## Step 3: Enable the Firewall

```bash
sudo ufw enable
sudo ufw status verbose
```

These commands activate UFW and display its current status.

## Step 4: Allow Web Application Traffic

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

These commands allow incoming TCP traffic on port 8080 and display the numbered firewall rules.

## Step 5: Test the Web Application

```bash
curl http://localhost:8080
curl -I http://localhost:8080
```

These commands test whether the Nginx application responds locally.

## Important SSH Security Reminder

Enabling UFW before allowing SSH could block remote administrative access and lock an administrator out of the server.

## Security Observation

The Default Deny policy reduces unnecessary network exposure. However, Docker-published ports may bypass ordinary UFW incoming rules, and a localhost curl test does not prove external traffic is filtered.

## Final Verification

Record the actual firewall status and any errors observed during the KillerCoda session before submitting this report.
