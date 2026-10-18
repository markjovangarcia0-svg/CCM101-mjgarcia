# Laboratory Activity 8: The Cloud Security Engineer

## Mission Overview

This laboratory focuses on improving cloud server security using the Uncomplicated Firewall (UFW) on Ubuntu. The activity includes deploying an Nginx application, auditing network ports, configuring firewall policies, and allowing only the required services.

## Objectives

- Understand the Principle of Least Privilege and attack surfaces.
- Audit listening network ports on Ubuntu.
- Configure a Default Deny firewall policy.
- Allow SSH access on port 22.
- Allow web application traffic on TCP port 8080.
- Document security procedures and observations.

## Commands Executed

```bash
docker run -d --name secure-web-app -p 8080:80 nginx:alpine
docker ps
curl http://localhost:8080
sudo ss -tuln
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl -I http://localhost:8080
```

## Skills Learned

- Linux network auditing
- Basic Docker container deployment
- UFW firewall configuration
- Network port management
- SSH and HTTP security awareness
- Cloud security documentation

## Screenshot Evidence

1. `screenshots/vulnerable-app-running.png` — Initial Nginx curl response.
2. `screenshots/firewall-activated.png` — Active UFW firewall and Default Deny policy.
3. `screenshots/firewall-port-allowed.png` — Allowed port 8080 and successful curl response.

Screenshot files will be added manually to GitHub.

## Security Note

Local application connectivity does not by itself verify external firewall filtering. Docker networking may require additional controls.

## Conclusion

This laboratory demonstrates the importance of limiting network access, reviewing exposed services, and documenting security configurations as part of cloud server administration.
